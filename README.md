# 1. Review Analysis Report

## 1. Overview
- This project utilizes Selenium to scrape reviews for various accommodation types (motels, hotels, guesthouses, pensions/villas) and stores the reviews in text files. The stored reviews are then analyzed for the frequency of nouns and verbs, and the results are presented.

## 2. Review Scraping and Storage
- Reviews are scraped using the `{AccommodationType}ReviewScraper` class, which uses Selenium to gather up to 100 reviews for each accommodation type (motels, hotels, guesthouses, pensions/villas).
- The scraped reviews are saved in text files, with the path being 'scrap_data/{AccommodationName}/reviews.txt'.

## 3. Frequency Analysis of Nouns and Verbs
- To analyze the frequency of nouns and verbs in the scraped reviews, the Konlpy library is used. This allows for the extraction of nouns and verbs from Korean text, and the Counter module is used to calculate the frequency of each word.
- The results of the analysis are stored in a text file at 'scrap_data/{AccommodationNames}/nouns_and_verbs.txt'.

## 4. Frequency Plots and Word Clouds
- Frequency plots and word clouds are generated for nouns and verbs for each accommodation type. The frequency data is used to create plots and word clouds for each accommodation.
- The generated image files are saved in 'scrap_data/{AccommodationName}/nouns' and 'scrap_data/{AccommodationName}/verbs'.

## 5. Conclusion
- The analysis reveals the most frequently mentioned nouns and verbs in reviews for different accommodation types (motels, hotels, guesthouses, pensions/villas).
- These insights provide a deeper understanding of the features and services of each accommodation type and will help in analyzing customer satisfaction and demands.

# 2. Vectorization Report

## 1. Overview
- To apply machine learning and deep learning, the collected review data was processed using countVectorization. The original reviews were cleaned and vectorized using nouns, and the code for this process differs from other methods due to the additional preprocessing steps.

## 2. Data Collection
- The text data for analysis is stored in the "{AccommodationType}_review.txt" file. Reviews are read from this file and used for analysis.

## 3. Data Preprocessing
1. Non-Korean characters are removed from the review data.
2. The reviews are split based on the phrase 'nth review.'.
3. Stopwords are removed, and morphological analysis is performed on the split reviews.

## 4. Morphological Analysis
1. The Okt morphological analyzer from KoNLPy is used for POS tagging.
2. Nouns and verbs are extracted, and their base forms are retrieved.

## 5. Stopword Removal
- Stopwords are loaded from a text file, which is used to filter out unnecessary words from the reviews during analysis.

## 6. Results
- The result of this process is a cleaned set of review data, ready for analysis.

## 7. Document-Term Matrix (DTM) Creation
- A document-term matrix (DTM) is created using CountVectorizer.
- DTM represents the frequency of words in each document and can be used for further analysis.
