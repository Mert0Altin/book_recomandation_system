# book_recomandation_system
video: https://youtu.be/7kFAqVl6EAo

Description
This project scrapes book ratings and related information from the website 1000kitap.com, stores the data in a CSV file, and then applies machine learning models to predict book ratings. The project is divided into two parts: web scraping and machine learning.

Requirements
selenium
beautifulsoup4
webdriver-manager
pandas
numpy
scikit-learn
matplotlib
seaborn
Install these dependencies using the following: pip install selenium beautifulsoup4 webdriver-manager pandas numpy scikit-learn matplotlib seaborn

Web Scraping Part
This part of the project involves scraping book ratings from user profiles on 1000kitap.com.

extract_urls(page_num)
This function extracts URLs from pages containing user book ratings. It uses Selenium and BeautifulSoup to extract the URLs.

Main Web Scraping Loop
Loops through multiple pages and extracts book ratings for each user.
Avoids scraping users whose profiles are private or restricted.
Writes the scraped data (book name and user rating) to a CSV file.
Machine Learning Part
The second part of the project uses the scraped data to build machine learning models that predict user ratings for books.

load_and_prepare_data(data)
Prepares the data by encoding categorical variables and converting data types. It returns a Pandas DataFrame with kullanici_id, kitap_id, and puan (rating).

analyze_data(df)
Performs basic data analysis:

Descriptive statistics of ratings.
Average ratings per user.
train_and_evaluate_models(df)
Trains three machine learning models (KNN, Random Forest, and SVR) to predict user ratings for books and evaluates their performance using metrics such as:

Mean Squared Error (MSE)
Mean Absolute Error (MAE)
R-squared (R2)
How to Run
Run the web scraping part to gather data and save it in a CSV file.
Load the CSV file and run the machine learning part to train models and make predictions.
Output
The CSV file with user ratings for books.
Model performance metrics (MSE, MAE, R2) for each of the models.
Example Output:
Kitap Adı: Kitap1, Kullanıcı Puanı: 8
Kitap Adı: Kitap2, Kullanıcı Puanı: 9
...
Notes
The scraper uses a headless version of Chrome for efficient data collection.
Data is saved incrementally to avoid overwriting previous results.
