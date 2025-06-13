Corporate Value Analyzer
A web-based prototype designed to analyze a company's stated mission values against the sentiment of its employee reviews. This tool serves as a "reality check" to see if a company's culture aligns with its marketing.

This project was built as a self-contained HTML file to demonstrate the core logic of scraping, sentiment analysis, and comparison in a simple, easy-to-understand format. It's perfect for learning, reverse-engineering, and building upon.

How It Works: The Core Concept
The application operates on a simple three-step logic:

Extract Keywords: The user provides a list of keywords from a company's mission or values statement (e.g., "innovation," "integrity," "collaboration").

Analyze Reviews: The user pastes a collection of employee reviews. The application then performs a basic sentiment analysis on each review to determine if its tone is generally positive, negative, or neutral.

Generate a Scorecard: For each keyword, the tool finds all reviews that mention it and calculates the average sentiment score. This produces a "Reality Check Scorecard" that directly compares the company's promises to the employees' experiences.

How to Use This Prototype
Since this is a single, self-contained index.html file, using it is simple:

Save the Code: Save the provided HTML code as index.html.

Open in Browser: Open the index.html file in any modern web browser (like Chrome, Firefox, or Edge).

Enter Keywords: In the first input box, type the core values from a company's mission statement, separated by commas.

Paste Reviews: Find a few employee reviews for that company (from Glassdoor, Indeed, etc.) and paste them into the large text area. Each review should be on a new line.

Analyze: Click the "Analyze Values" button to generate the scorecard and see the results!

Technology Used
This prototype is intentionally kept simple to focus on the core logic.

HTML: For the structure of the application.

Tailwind CSS: For all styling, providing a clean, modern, dark-mode UI without needing a separate CSS file.

JavaScript (Vanilla): For all the application logic, including:

DOM manipulation (reading inputs, displaying results).

A simple, lexicon-based sentiment analysis function for demonstration purposes.

For Reverse-Engineering: From Prototype to Production
This HTML file is a great starting point, but it has one major limitation: it cannot perform live web scraping. Due to browser security policies (CORS), JavaScript running in a browser is blocked from making requests to other websites like Glassdoor.

To build a real-world version of this tool, you would move the scraping and analysis logic to a backend server. Here’s what that would look like:

Backend (Python Example):

Framework: Use a web framework like Flask or Django to create an API.

Web Scraping: Use libraries like Selenium (to control a browser and handle dynamic JavaScript) and BeautifulSoup (to parse the HTML) to automatically fetch the reviews from Glassdoor instead of having the user paste them.

NLP / Sentiment Analysis: Instead of the simple lexicon, use a powerful NLP library like TextBlob, VADER, or spaCy for much more accurate sentiment analysis.

API Endpoint: Your Python backend would have an endpoint that your frontend could call. The frontend would send a company name, and the backend would do all the scraping and analysis, returning a clean JSON object with the final scorecard.

Frontend (What you have now):

The frontend would be modified to call your new backend API instead of performing the analysis itself. It would display a loading state while the server works and then render the results it receives from the API.

Future Improvements
If you wanted to take this project even further, here are some ideas:

Automate Keyword Extraction: Use NLP techniques to automatically identify the key values from a pasted mission statement.

Advanced Sentiment Analysis: Implement Aspect-Based Sentiment Analysis (ABSA) to understand the sentiment towards a specific keyword within a sentence.

Data Visualization: Use a library like Chart.js to create bar charts or graphs to visualize the sentiment scores for each value.

Historical Analysis: Scrape and store reviews over time to track if a company's culture is improving or declining.
