# 🎬 IMDb Web Scraping Project

## 📌 Project Overview
This project demonstrates how to scrape movie data from the **IMDb Top Movies** page using Python. The goal is to practice fundamental web scraping skills, including inspecting website structure, extracting data from HTML pages, handling common scraping challenges, and storing the results in a structured format for analysis.



---

## 🎯 Objectives
The project was completed based on the following instructions:

- Identify a target website and inspect its HTML structure
- Use **BeautifulSoup** and **requests** to scrape data from web pages
- Store scraped data in a structured format (CSV)
- Handle common challenges such as pagination and dynamic content

---

## 🌐 Target Website
**Website:** IMDb Top 250 Movies  
🔗 https://www.imdb.com/chart/top/

### Why IMDb?
- Publicly accessible page
- Contains well-structured movie data
- Suitable for learning basic web scraping techniques



---

## 🧰 Tools & Technologies
- **Python** – Programming language
- **requests** – To send HTTP requests
- **BeautifulSoup** – To parse and extract HTML content
- **pandas** – To structure, clean, and store data

---

## 🔍 Website Inspection
Using browser developer tools, the following structure was identified:

- Each movie is contained inside an HTML element:
  ```html
  <li class="ipc-metadata-list-summary-item">
  ```
- Movie title is found in:
  ```html
  <h3>
  ```
- Movie rating is found in:
  ```html
  <span class="ipc-rating-star">
  ```

This repeating structure makes it possible to extract multiple movies programmatically.

---

## 🧪 Methodology

### 1. Sending Requests
A GET request is sent to the IMDb Top Movies page using the `requests` library. A **User-Agent header** is included to simulate a real browser and avoid request blocking.

### 2. Parsing HTML
The page content is parsed using **BeautifulSoup**, converting raw HTML into a searchable structure.

### 3. Data Extraction
For each movie, the following data is extracted:
- Movie title
- IMDb rating

### 4. Data Storage
The extracted data is:
- Stored temporarily in a Python list of dictionaries
- Converted into a pandas DataFrame
- Exported as a **CSV file** for further analysis

---

## 📄 Output
The final dataset is saved as:
imdp_top_action.csv
TopIDMb_Movies.csv
```

Sample columns:
- `Title`
- `Rating`

---

## 🔁 Handling Common Challenges

### Pagination
- The IMDb Top 250 movies are displayed on a **single page**
- The Movie (Avatar: Fire and Ash) displayed on the page is a dynamic content. 
  It was handled using Selenium

### Dynamic Content
- IMDb uses JavaScript for many pages
- `requests` cannot render JavaScript

**How this was handled:**
- Only the Top Movies page was scraped, as its data is available in the initial HTML
- For fully dynamic pages, tools such as **Selenium** or IMDb datasets are recommended

---


---

## 🚀 Future Improvements
Possible enhancements include:
- Extracting additional fields (year, movie links)
- Cleaning and converting ratings to numeric values
- Using Selenium for dynamic IMDb pages
- Analyzing IMDb datasets for large-scale projects
- Creating visualizations using matplotlib or seaborn

---

## 📚 Learning Outcomes
Through this project, the following skills were practiced:
- HTML inspection and structure analysis
- Web scraping with Python
- Handling real-world scraping limitations
- Data structuring using pandas
- Exporting data for analysis

---

## 👤 Author
**Project completed as part of a internship exercise.**

---


