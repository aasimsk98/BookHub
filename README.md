# BookHub: A Content-Based Book Recommender
---

## Live Application [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://worldofbooks.streamlit.app/)

You can access and use the live application here: **https://worldofbooks.streamlit.app/**

BookHub is an interactive web application that provides personalized book recommendations. It uses a content-based filtering approach, analyzing book titles and engineered features to find the books most similar to your selection.

The app features two distinct recommendation engines:
1.  **Overall Library:** A general recommender built on a dataset of over 220,000 book records.
2.  **Exclusive MU Engineering Library:** A specialized recommender for engineering students, using domain-specific features (like semester, subject, and keywords) for highly relevant suggestions.
---

## Tech Stack

* **Python:** Core programming language.
* **Streamlit:** For building and deploying the interactive web application.
* **Scikit-learn:** For implementing the TF-IDF Vectorizer and calculating Cosine Similarity.
* **Pandas & NumPy:** For all data manipulation, preprocessing, and calculations.
* **Pillow (PIL):** For loading the logo image in the UI.

---

## Repository Structure

* **`app.py`**: The main Streamlit web application script that contains all UI and backend logic.
* **`requirements.txt`**: A list of all Python libraries required to run the project.
* **`item_based.csv`**: The primary dataset containing over 220,000 book records.
* **`item_based1.csv`**: The specialized dataset for the engineering library, with custom features.
* **`logo.png`**: The BookHub logo image file displayed in the Streamlit interface.
* **`README.md`**: This documentation file.

## How to Run Locally

You can run this project on your local machine by following these steps:

**1. Clone the Repository**
```bash
git clone https://github.com/aasimsk98/BookHub.git
cd BookHub
```

**2. Create a Virtual Environment (Recommended)**

```
Bash
# For macOS/Linux
python3 -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
.\venv\Scripts\activate
```
**3. Install Dependencies**

This project's dependencies are listed in requirements.txt.
```
Bash
pip install -r requirements.txt
```
**4. Run the Streamlit App**
```
Bash
streamlit run app.py
```
The application will automatically open in your web browser.

**Note on Data:** The app fetches the required CSV datasets directly from GitHub. If you wish to run this offline:
 
In `app.py`, change lines 16 and 17 to read from the local files:
    ```python
    Item_based = pd.read_csv('item_based.csv')
    Item_based1 = pd.read_csv('item_based1.csv')
    ```
