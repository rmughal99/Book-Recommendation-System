
---

# Book Recommendation System

## Introduction
This project is a **Book Recommendation System** built using collaborative filtering techniques. It recommends books based on user input by leveraging similarity scores and displays a list of popular books. The system is implemented with **Flask** as the backend and **Bootstrap** for a responsive, clean UI. The recommendation model uses pre-trained data for efficient predictions.

## Features

- **Popular Books Display**: The homepage shows the top 50 popular books with their titles, authors, number of votes, and average ratings.
- **Book Recommendation**: Based on a user’s input, the system suggests similar books using a pre-trained similarity score model.
- **Interactive UI**: A Bootstrap-styled interface ensures an intuitive and responsive user experience.

## Dataset

- **Kaggle Link**: https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/data
  
The dataset includes:
- **Books**: Titles, authors, and images.
- **Ratings**: User ratings for various books.
- **User Data**: Anonymous user interaction data with books.

If you are using a publicly available dataset, mention its source, such as **Goodreads** or **Kaggle**. You can also include any preprocessing steps like data cleaning or modifications to the dataset.

## Methodology

1. **Data Preprocessing**:
   - A **pivot table** is created where rows represent users, columns represent books, and the values represent user ratings.
   - Missing values are handled by either imputing them with zeros or calculating the mean rating.

2. **Collaborative Filtering**:
   - The model uses **item-based collaborative filtering** to recommend books based on user ratings.
   - **Cosine Similarity** is computed to measure the similarity between books based on their rating patterns.

3. **Recommendation Generation**:
   - For a given book, cosine similarity scores with all other books are computed, and a list of top N most similar books is returned.



## Installation and Setup

### Prerequisites
Ensure the following libraries are installed:
```bash
pip install flask numpy pandas pickle-mixin scikit-learn
```

### Steps to Run the Application

   ```
# first Activate virual environment using .\env\Scripts\Activate 
1 **Install Dependencies**:
   Install the required Python packages by running:
   ```bash
   pip install -r requirements.txt
   ```

2. **Prepare Model Files**:
   Ensure the following files are available in the `models/` directory:
   - `popular.pkl`
   - `pt.pkl`
   - `books.pkl`
   - `similarity_scores.pkl`

3 **Run the Application**:
 
   python app.py
   ```




## Model and Data Files

### Pre-trained Models:
- **Popular Books Model (`popular.pkl`)**: Contains data on the most popular books.
- **Pivot Table (`pt.pkl`)**: Used to compute book-to-book similarities.
- **Books Metadata (`books.pkl`)**: Includes information about book titles, authors, and images.
- **Similarity Scores (`similarity_scores.pkl`)**: Precomputed similarity scores between books for faster recommendations.

### Model Training:
- **Cosine Similarity** is used to compute the similarity between books based on user ratings.
- A **pivot table** is constructed from the user-book interaction data to calculate these similarity scores.

## Technologies Used

- **Backend**: Flask (Python)
- **Frontend**: HTML, CSS (Bootstrap)
- **Data Processing**: Numpy, Pandas, Scikit-learn
- **Model Persistence**: Pickle




---
