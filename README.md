# Mark-2 Scaper - User Guide

A powerful contact information scraper that automates Google searches to extract email addresses and phone numbers from various online sources including social media platforms, business directories, and websites.

## Quick Start Guide

### Step 1: Prerequisites Check
- ✅ Windows 10 or later
- ✅ .NET Framework 4.8 installed
- ✅ Google Chrome browser installed
- ✅ Internet connection

### Step 2: Get the Application
1. Download or clone the project source code
2. Open `Mark_2 Scaper.csproj` in Visual Studio 2019 or later
3. Wait for NuGet packages to restore automatically
4. Build the solution (F6 or Build → Build Solution)

### Step 3: Run the Application
1. Press F5 to start debugging, or
2. Navigate to `bin\Debug\` folder and run `Mark_1 Scaper.exe`

### Step 4: Configure Your First Scrape
1. **Enter Keyword**: Type your search term (e.g., "restaurant in New York")
2. **Output File**: Enter filename like "contacts.csv" or "leads.xlsx"
3. **Pages**: Set to 3-5 pages per query (start small)
4. **Proxy**: Check if you want to use proxy (optional)

### Step 5: Select Data Sources
Choose platforms to search:
- ☑️ Facebook, Instagram, LinkedIn for social contacts
- ☑️ IndiaMart, Justdial for business directories
- ☑️ Website for general web results

### Step 6: Select Contact Types
Choose what to extract:
- ☑️ Gmail - for Google email addresses
- ☑️ Outlook - for Microsoft emails
- ☑️ Phone - for phone numbers

### Step 7: Start Scraping
1. Click **"Start Scraping"** button
2. Watch the logs for progress
3. Wait for completion message
4. Check your Documents\Mark1_Scraper\ folder for results

## Detailed Features

- **Automated Google Search**: Uses Selenium WebDriver to perform targeted Google searches
- **Multiple Data Sources**: Supports scraping from:
  - Social Media: Facebook, Instagram, YouTube, LinkedIn, Twitter, TikTok, Tumblr, Pinterest, Reddit
  - Business Directories: IndiaMart, Justdial, TradeIndia, ExportersIndia
  - Other: Websites, PDF files
- **Contact Types**: Extracts Gmail addresses, Outlook emails, and phone numbers
- **Proxy Support**: Optional proxy configuration for enhanced anonymity
- **Captcha Handling**: Manual captcha solving with user notification
- **Excel/CSV Output**: Saves results in structured spreadsheet format
- **Multi-page Scraping**: Configurable number of Google result pages to process
- **Real-time Logging**: Live progress updates and error reporting
- **Cancellation Support**: Ability to stop scraping operations mid-process

## Requirements

- **Operating System**: Windows 10 or later
- **.NET Framework**: Version 4.8 or higher
- **Google Chrome Browser**: Latest version recommended
- **Internet Connection**: Required for web scraping operations

## Dependencies

The application uses the following NuGet packages:

- **Selenium.WebDriver** (4.39.0) - Browser automation
- **Selenium.WebDriver.ChromeDriver** (143.0.7499.16900) - Chrome driver
- **ClosedXML** (0.105.0) - Excel file manipulation
- **CommunityToolkit.WinUI.Notifications** (7.1.2) - Windows notifications
- **DocumentFormat.OpenXml** (3.1.1) - Office document handling
- Various system libraries for enhanced compatibility

## Installation (Detailed)

1. **Clone or Download**: Obtain the project source code
2. **Open in Visual Studio**: Load `Mark_2 Scaper.csproj` in Visual Studio 2019 or later
3. **Restore NuGet Packages**: Visual Studio should automatically restore packages, or run:
   ```
   nuget restore Mark_2 Scaper.csproj
   ```
4. **Build Solution**: Build the project in Debug or Release configuration

## Usage Guide

### Application Interface
The main window contains:
- **Keyword field**: Enter your search terms
- **Output file field**: Name your results file (.csv or .xlsx)
- **Pages control**: Number of Google pages to scrape (1-100)
- **Proxy checkbox**: Enable proxy for anonymity
- **Sources checkboxes**: Select platforms to search
- **Query Types checkboxes**: Select Gmail/Outlook/Phone
- **Start/Stop buttons**: Control scraping process
- **Logs area**: Real-time progress and status messages

### Running a Scrape Operation

1. **Launch Application**: Run the compiled executable or start debugging in Visual Studio
2. **Configure Search**:
   - Enter search keyword(s)
   - Specify output filename (CSV or XLSX)
   - Set number of pages to scrape per query (1-100)
   - Optionally enable proxy usage
3. **Select Data Sources**: Choose from available platforms and directories
4. **Select Contact Types**: Choose Gmail, Outlook, and/or Phone extraction
5. **Start Scraping**: Click "Start Scraping" button
6. **Monitor Progress**: Watch real-time logs for progress updates
7. **Stop if Needed**: Use "Stop" button to cancel operation

### Understanding the Logs
- ▶ **Started**: Scraping operation begins
- 🌐 **Chrome opened**: Browser initialized
- 📄 **Page X**: Processing Google result page X
- 🔗 **Found Y results**: Number of search results on current page
- 📧 **X emails | 📞 Y phones**: Contacts extracted from page
- ✅ **Completed**: Operation finished successfully
- ❌ **Error**: Something went wrong

## Output Format

Results are saved to a CSV or Excel file in `Documents\Mark1_Scraper\` folder with the following columns:

- **Keyword**: The search term used
- **Source**: Platform where contact was found (e.g., facebook.com)
- **Signal**: Type of contact (gmail/outlook/phone)
- **Title**: Google search result title
- **Snippet**: Preview text from search result
- **URL**: Full URL of the result
- **Domain**: Website domain
- **Emails**: Extracted email addresses (comma-separated)
- **Phones**: Extracted phone numbers (comma-separated)
- **GooglePage**: Page number where result was found

## Tips for Best Results

- **Start Small**: Begin with 2-3 pages and one source to test
- **Use Specific Keywords**: "restaurant supply company" better than "restaurant"
- **Combine Sources**: Check multiple platforms for comprehensive results
- **Monitor Logs**: Watch for captcha prompts or errors
- **Save Regularly**: Use different filenames for different searches

## Important Notes

- **Legal Compliance**: Ensure compliance with website terms of service and applicable laws regarding web scraping
- **Rate Limiting**: Built-in delays prevent overwhelming target websites
- **Captcha Handling**: Manual intervention required if Google presents captchas
- **Proxy Configuration**: Modify proxy settings in `BrowserManager.cs` if needed
- **Error Handling**: Application includes robust error handling and recovery mechanisms

## Architecture

The application follows a modular architecture:

- **MainForm.cs**: User interface and main application logic
- **Cores/**: Core scraping components
  - `BrowserManager.cs`: Chrome browser automation
  - `GoogleNavigator.cs`: Google search orchestration
  - `GoogleResultParser.cs`: Search result parsing
  - `ContactExtractor.cs`: Email/phone extraction logic
  - `ExcelWriter.cs`: Output file generation
  - `CaptchaHandler.cs`: Captcha detection and handling
  - `ProxyManager.cs`: Proxy configuration
- **Model/**: Data structures for queries and results
- **Util/**: Utility classes for logging and notifications

## Troubleshooting

- **Chrome Driver Issues**: Ensure Chrome browser is updated and compatible
- **Proxy Problems**: Verify proxy server settings and connectivity
- **File Access Errors**: Ensure write permissions to output directory
- **Captcha Loops**: Manual captcha solving may be required periodically
- **No Results Found**: Try different keywords or sources
- **Application Won't Start**: Check .NET Framework installation

## License

This project is provided as-is for educational and research purposes. Please review and comply with all applicable laws and terms of service.</content>
<parameter name="filePath">c:\Users\4394\source\repos\Mark_2 Scaper\README.md
