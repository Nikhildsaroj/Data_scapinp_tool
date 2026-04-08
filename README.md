# Mark-2 Scaper

A powerful contact information scraper that automates Google searches to extract email addresses and phone numbers from various online sources including social media platforms, business directories, and websites.

## Features

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

## Installation

1. **Clone or Download**: Obtain the project source code
2. **Open in Visual Studio**: Load `Mark_2 Scaper.csproj` in Visual Studio 2019 or later
3. **Restore NuGet Packages**: Visual Studio should automatically restore packages, or run:
   ```
   nuget restore Mark_2 Scaper.csproj
   ```
4. **Build Solution**: Build the project in Debug or Release configuration

## Usage

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

## License

This project is provided as-is for educational and research purposes. Please review and comply with all applicable laws and terms of service.</content>
<parameter name="filePath">c:\Users\4394\source\repos\Mark_2 Scaper\README.md
