# Enhanced Web Scraper

A robust, production-ready web scraper built with Python that extracts structured data from websites with advanced features like retry logic, multiple export formats, and comprehensive logging.

## 🚀 Features

### Core Functionality
- **Smart Retry Logic**: Automatic retry with exponential backoff for failed requests
- **Session Management**: Persistent sessions for better performance
- **Rate Limiting**: Built-in delays to respect server resources
- **Comprehensive Logging**: Detailed logs for debugging and monitoring

### Data Extraction
- ✅ **Headings**: All heading levels (H1-H6) with hierarchy
- ✅ **Links**: Internal and external links with classification
- ✅ **Images**: Image URLs with alt text and titles
- ✅ **Tables**: Structured table data extraction
- ✅ **Metadata**: Page title, meta tags, and SEO information

### Export Formats
- 📄 **JSON**: Complete structured data
- 📊 **CSV**: Tabular data for analysis
- 📝 **TXT**: Plain text output
- 📋 **Logs**: Detailed execution logs

## 📋 Requirements

- Python 3.7+
- See `requirements.txt` for dependencies

## 🔧 Installation

1. Clone or download the project files
2. Install dependencies:
```bash
pip install -r requirements.txt
```

## 💻 Usage

### Basic Usage

```python
from enhanced_scraper import WebScraper

# Initialize scraper
scraper = WebScraper(base_url='https://example.com', max_retries=3)

# Scrape a page
data = scraper.scrape_page('https://example.com', extract_all=True)

# Save data
scraper.save_to_json(data, 'output.json')
scraper.save_to_csv(data['headings'], 'headings.csv')
```

### Running the Example

```bash
python enhanced_scraper.py
```

This will scrape the default Wikipedia page and save data to the `scraped_data/` directory.

## 📊 Output Structure

### JSON Output
```json
{
  "url": "https://example.com",
  "timestamp": "2024-02-09T10:30:00",
  "metadata": {
    "title": "Page Title",
    "description": "Page description"
  },
  "headings": [
    {
      "level": "h2",
      "text": "Heading Text",
      "id": "heading-id"
    }
  ],
  "links": [...],
  "images": [...],
  "tables": [...]
}
```

## 🎯 Key Improvements Over Original

### 1. **Object-Oriented Design**
- Cleaner, more maintainable code
- Reusable scraper class
- Better organization

### 2. **Enhanced Error Handling**
- Retry logic with exponential backoff
- Specific exception handling
- Graceful degradation

### 3. **Advanced Features**
- Extract multiple data types (headings, links, images, tables)
- Metadata extraction
- Link classification (internal/external)
- Multiple export formats

### 4. **Better Logging**
- File and console logging
- Different log levels
- Timestamp tracking
- Execution statistics

### 5. **Production-Ready**
- Type hints for better code clarity
- Comprehensive docstrings
- Configuration file support
- Directory structure management

### 6. **Performance Optimization**
- Session reuse
- Configurable timeouts
- Rate limiting
- Exponential backoff

## 🛠️ Configuration

Edit `scraper_config.ini` to customize:
- Target URLs
- Retry settings
- Output formats
- Logging preferences

## 📁 Project Structure

```
web-scraper/
├── enhanced_scraper.py      # Main scraper class
├── scraper_config.ini       # Configuration file
├── requirements.txt         # Dependencies
├── README.md               # Documentation
├── scraper.log             # Execution logs
└── scraped_data/           # Output directory
    ├── scraped_data_*.json
    ├── headings_*.csv
    ├── links_*.csv
    └── images_*.csv
```

## 🔍 Use Cases

- **SEO Analysis**: Extract metadata and heading structure
- **Content Aggregation**: Collect articles from multiple sources
- **Link Analysis**: Map internal and external link structures
- **Data Mining**: Extract structured data from web pages
- **Research**: Gather information from academic or news websites

## ⚠️ Best Practices

1. **Respect robots.txt**: Always check site's robots.txt
2. **Rate Limiting**: Don't overwhelm servers with requests
3. **User-Agent**: Use descriptive User-Agent strings
4. **Terms of Service**: Follow website's ToS
5. **Legal Compliance**: Ensure scraping is legal for your use case

## 🚧 Future Enhancements

- [ ] Multi-threaded scraping
- [ ] Proxy support
- [ ] JavaScript rendering (Selenium/Playwright)
- [ ] Database integration (SQLite/PostgreSQL)
- [ ] API mode with Flask/FastAPI
- [ ] Scheduled scraping (cron jobs)
- [ ] Data validation and cleaning
- [ ] Email notifications
- [ ] Cloud storage integration (AWS S3, Google Cloud)

## 📝 License

This project is open source and available for educational purposes.

## 👤 Author

**Shivam Singh**
- Email: shivamsingh13c@gmail.com
- LinkedIn: [Shivam Singh](https://linkedin.com/in/shivam-singh)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

---

**Note**: Always ensure you have permission to scrape a website and follow ethical scraping practices.
