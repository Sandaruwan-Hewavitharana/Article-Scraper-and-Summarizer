### **Overview**

This is a lightweight web application built with Python and the Flask framework that provides concise, AI-generated summaries of news articles. It's designed to help users quickly grasp the key points of a story without having to read the entire article. The application uses a custom web scraping tool to fetch article content and the powerful Google Gemini API to perform the summarization.

![image alt](https://github.com/Sandaruwan-Hewavitharana/Article-Scraper-and-Summarizer/blob/b37f393abb2ec6cab6fe5f47961ff541b9cc4f2b/127.0.0.1_5000_(Nest%20Hub%20Max).png)

### **Key Features**

  * **AI-Powered Summarization**: Utilizes the Google Gemini AI model to generate human-like, 3-4 sentence summaries of articles.
  * **Dynamic Web Scraping**: Scrapes and fetches the full content of news articles from a specified source (`bbc.com/innovation/technology`) using the `newspaper3k` library.
  * **Simple Web Interface**: A clean and easy-to-use web interface built with Flask that displays headlines with images and provides a dedicated page for each summarized article.
  * **In-Memory Caching**: Improves performance by caching recently scraped article content, avoiding redundant scraping when a user clicks on a headline.
  * **Modular Codebase**: The project is organized into distinct, well-documented components (`app.py`, `scraper.py`, `summarizer.py`) for clarity and maintainability.

### **Technologies Used**

  * **Backend**: Python, Flask
  * **Web Scraping**: `requests`, `beautifulsoup4`, `newspaper3k`
  * **AI/LLM**: Google Gemini API via the `google-generativeai` library
  * **Frontend**: HTML, CSS

![image alt](https://github.com/Sandaruwan-Hewavitharana/Article-Scraper-and-Summarizer/blob/bd0972cabf4d461767c3d38b77967e25ff1a596f/127.0.0.1_5000_article_url%3Dhttps___www.bbc.com_travel_to-the-ends-of-the-earth(Nest%20Hub%20Max).png)

### **Setup and Installation**

To get this project up and running on your local machine, follow these steps.

1.  **Clone the Repository**

    ```
    git clone [your-repo-url]
    cd [your-repo-name]
    ```

2.  **Set up a Virtual Environment**
    It's best practice to use a virtual environment to manage project dependencies.

    ```
    python -m venv venv
    # On macOS/Linux
    source venv/bin/activate
    # On Windows
    venv\Scripts\activate
    ```

3.  **Install Dependencies**
    The project uses a `requirements.txt` file to list all necessary libraries.

    ```
    pip install -r requirements.txt
    ```

4.  **Configure Your API Key**
    You need a Google Gemini API key to run the summarizer.

      * Get a key from [Google AI Studio](https://aistudio.google.com/app/apikey).
      * Set it as an environment variable in your terminal.
          * On macOS/Linux: `export GEMINI_API_KEY='YOUR_API_KEY'`
          * On Windows: `set GEMINI_API_KEY=YOUR_API_KEY`

5.  **Run the Application**
    Start the Flask web server.

    ```
    python app.py
    ```

    The application will run at `http://127.0.0.1:5000`.

