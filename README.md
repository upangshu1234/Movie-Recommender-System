# 🎬 Movie Recommender System

A content-based movie recommender system built using machine learning and deployed using Streamlit. This app suggests movies based on textual metadata like genres, cast, crew, keywords, and overview.


---

## 📁 Dataset

Used the **TMDB 5000 Movie Dataset** from Kaggle:  
🔗 [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## 📌 Features

- Content-based filtering using movie metadata.
- Displays top 5 recommended movies.
- Fetches movie posters using TMDB API.
- Simple and interactive UI with Streamlit.

---

## 🧠 How It Works

1. **Data Preprocessing:**  
   - Combined relevant features: `overview`, `genres`, `keywords`, `cast`, `crew`.
   - Cleaned and merged textual data into a single feature column: `tags`.

2. **Vectorization:**  
   - Converted `tags` to numerical data using `CountVectorizer` (Bag of Words approach).

3. **Similarity Calculation:**  
   - Computed cosine similarity between all movie vectors.

4. **Recommendation:**  
   - When a user selects a movie, top 5 similar movies are displayed with posters.

---

## 🛠️ Installation & Usage

### Clone the repo
```bash
git clone https://github.com/yourusername/movie-recommender-system.git
cd movie-recommender-system
````

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the app

```bash
streamlit run app.py
```

---

## 🧾 Requirements

Save this in `requirements.txt`:

```txt
streamlit
scikit-learn
pandas
numpy
requests
```

---

## 🗝️ TMDB API Key

This app uses the TMDB API to fetch movie posters. The current code uses a sample key. For your own usage:

1. Sign up at [https://www.themoviedb.org/](https://www.themoviedb.org/)
2. Go to your API settings and generate an API key.
3. Replace the key in `app.py`:

```python
url = f"https://api.themoviedb.org/3/movie/{movie_id}?api_key=YOUR_API_KEY&language=en-US"
```

---

## 📒 Files

| File               | Description                                 |
| ------------------ | ------------------------------------------- |
| `app.py`           | Streamlit app                               |
| `notebook.ipynb`   | Data preprocessing and model training       |
| `movie_list.pkl`   | Pickled DataFrame containing movie metadata |
| `similarity.pkl`   | Pickled cosine similarity matrix            |
| `requirements.txt` | Python dependencies                         |
| `README.md`        | This file                                   |

---

## 📸 Screenshots

*(Optional) Add a screenshot or two of your app running to help others understand what it looks like.*

---

## ✍️ Author

Made with ❤️ by [Upangshu Basak](https://github.com/upangshu1234)

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

````

---

### ✅ To-Do Before Uploading

1. Replace `YOUR_API_KEY` if needed.
2. Add a `preview.png` screenshot inside the `assets/` folder (use `streamlit run app.py` and take a screenshot).
3. Create a `requirements.txt` using:
   ```bash
   pip freeze > requirements.txt
````

4. Create a `.gitignore` (optional but recommended):

   ```
   __pycache__/
   *.pkl
   .DS_Store
   ```

---
