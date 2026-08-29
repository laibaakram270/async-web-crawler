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
 git clone <your-repo-link>
cd async-web-crawler
