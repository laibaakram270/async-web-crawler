# Async Web Crawler & Data Extraction CLI Tool

A high-performance asynchronous web crawler built with Python 3.10+. This tool crawls websites, extracts page titles and URLs, and exports data to JSON/CSV while respecting rate limits and robots.txt.

## 🎯 Project Overview
This crawler implements all 4 modules required by DEV-NEXES:
1.  **Module 1: Async Scraping Pipeline** - `asyncio` + `HTTPX` for concurrent requests
2.  **Module 2: Rate Limiting + robots.txt** - Token Bucket algorithm for politeness
3.  **Module 3: Bloom Filter** - Memory-efficient duplicate URL detection
4.  **Module 4: CLI + Data Export** - `Click` CLI with JSON/CSV output

## 🛠️ Tech Stack & Dependencies

| Package | Version | Purpose |
| --- | --- | --- |
| **Python** | `3.9+` | Core language |
| **httpx** | `0.28.1` | Async HTTP client for fast web requests |
| **beautifulsoup4** | `4.15.0` | HTML parsing to extract titles and links |
| **soupsieve** | `2.9.2` | CSS selector engine for BeautifulSoup |
| **click** | `8.2.1` | Command Line Interface framework |
| **httpcore** | `1.0.9` | HTTPX dependency |
| **certifi** | `2026.7.22` | SSL certificates for HTTPS |

## ⚡ Installation Guide

### **Step 1: Prerequisites**
Make sure you have Python 3.9+ installed
```bash
python --version
```
## **Step 2: Clone or Download Project** ##
```bash
 git clone <https://github.com/laibaakram270/async-web-crawler>
cd async-web-crawler
```
## **Step 3: Install Dependencies** ##
```bash
bashpip install httpx beautifulsoup4 click
```
## **Step 4: Verify Installation** ##
```bash
python main.py --help
```
## **🚀 Usage** ##
Basic Command
```bash
python main.py --url <START_URL> --depth <DEPTH> --output <FILENAME>Examples
```
Crawl with depth 1 and save to JSON:
```bashp
ython main.py --url https://example.com --depth 1 --output data.json
```
Crawl with depth 3 and save to CSV:
```bash
python main.py --url https://example.com --depth 3 --output data.csv
```
## **📊 Example Output** ##
data.json:
```
[
  {
    "url": "https://example.com/",
    
    "title": "Example Domain"   
  }  
]
```
## **✅ Testing** ##
Run the crawler and check if data.json or data.csv is created in the folder.

## **🔑 Key Features** ##
1.AsyncIO + HTTPX: Handles multiple requests concurrently without blocking

2.Token Bucket: Limits to 2 requests per second to avoid overloading servers

3.Bloom Filter: Prevents re-crawling the same URL using minimal memory

4.robots.txt Compliance: Checks /robots.txt before crawling any domain

5.JSON/CSV Export: Flexible output for data analysis

