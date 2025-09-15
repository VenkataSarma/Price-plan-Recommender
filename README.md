
# Price Plan Recommendation System

## 🚀 Project Overview

The **Price Plan Recommendation System** is a web-based application designed to help telecom customers find the best-suited pricing plan based on their monthly usage patterns, including call minutes, SMS count, data usage, and OTT service preferences. The system leverages a data-driven approach using a combination of machine learning techniques, data preprocessing, and similarity measures to recommend the top 3 plans from a predefined dataset.

---

## 🎯 Features

- User-friendly web interface to input usage data
- OTT service preference selection (Netflix, Amazon Prime, Spotify, Hotstar, SonyLiv)
- Backend logic powered by Python Flask
- Recommendation logic based on weighted cosine similarity
- Displays detailed plan information and usage comparison charts
- Dark mode toggle for improved UX
- Reset form functionality for convenience

---

## 🛠️ Technology Stack

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Python Flask
- **Data Processing & ML Libraries:** 
    - Pandas
    - NumPy
    - scikit-learn
- **Similarity Calculation:** Cosine Similarity
- **UI Enhancements:** FontAwesome icons, Tailwind CSS
- **Deployment Ready:** Easily deployable on cloud platforms

---

## 📁 Project Structure

```
.
├── app.py                  # Flask application entry point
├── recommender.py          # Recommendation logic module
├── templates/
│   └── index.html          # Main frontend HTML template
├── tp.xlsx                 # Telecom plans dataset
├── static/                 # Folder for static files (CSS, JS, images)
├── README.md               # This file
└── requirements.txt        # Required Python dependencies
```

---

## 📊 Dataset Description

- `tp.xlsx` contains telecom plan details:
    - PlanID
    - MonthlyCost
    - IncludedMins
    - SMScount
    - IncludedatainGB
    - OTT (comma-separated OTT services)
    - PlanDescription

---

## ⚙️ How It Works

1. User enters monthly call minutes, SMS count, data usage (GB), and selects preferred OTT services.
2. Data is sent to the Flask backend via a POST request.
3. Backend loads the dataset and preprocesses the data using `StandardScaler`.
4. User input is transformed into a feature vector.
5. Weighted cosine similarity is calculated between user input and each plan’s feature vector.
6. The top 3 plans are selected based on similarity scores.
7. Recommendations are displayed on the frontend, with detailed information and comparison charts.

---

## ✅ Sample Usage

1. Launch the Flask server:
    ```bash
    python app.py
    ```
2. Open browser and navigate to:
    ```
    http://localhost:5000
    ```
3. Enter your usage data (calls, SMS, data) and select OTT preferences.
4. Click **See Recommendations** to get top 3 recommended plans.

---

## 🧱 Example Dataset Entry (`tp.xlsx`)

| PlanID | MonthlyCost | IncludedMins | SMScount | IncludedatainGB | OTT               | PlanDescription            |
|--------|------------|-------------|----------|----------------|-------------------|----------------------------|
| P1     | 299        | 1000        | 100      | 50             | Netflix,Hotstar   | Balanced plan for moderate users |
| P2     | 499        | 2000        | 200      | 100            | Amazon Prime      | Heavy usage plan with streaming services |

---

## 🚀 Future Enhancements

- Add real-time data integration from telecom provider APIs
- Implement Explainable AI to show reasoning behind recommendations
- Add user authentication and personalized history
- Include cross-selling suggestions for complementary services

---

## 📚 References

1. [scikit-learn cosine_similarity documentation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.cosine_similarity.html)
2. [Flask Web Framework](https://flask.palletsprojects.com/en/2.3.x/)
3. [React Official Site](https://reactjs.org/)
4. [Pandas Documentation](https://pandas.pydata.org/)

---

## 📄 License

MIT License

---

## 👨‍💻 Authors

- Venkata Sarma
