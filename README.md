# 📊 Linear Regression Model with Flask (50 Startups Dataset)

![Flask ML App](https://github.com/Careless-Caramel/prediction-using-flask/assets/86556401/ae55c877-350a-4db5-9216-90be64de9ff7)

This project integrates a **Linear Regression model** (trained on the *50 Startups dataset*) into a **Flask web application**.  
Users can interact with the model through a **web interface** or **API endpoint** to predict company profits based on input features.

---

## 🚀 Features

- ⚡ **Flask Web App** with user-friendly HTML form  
- 🤖 **Pre-trained Linear Regression Model** (stored as `model.pkl`)  
- 📩 **Form-based Prediction** (via web UI)  
- 🔗 **API Endpoint** (`/predict_api`) for programmatic access  
- 🛠️ Easy to extend for other ML models and datasets  

---

## 🛠️ Dependencies

- `Flask`
- `numpy`
- `scikit-learn`
- `pickle` (Python standard library)

Install dependencies with:

```bash
pip install flask numpy scikit-learn
```

---

## ⚙️ Installation

1. Clone the repository:

```bash
git clone https://github.com/Careless-Caramel/prediction-using-flask.git
cd prediction-using-flask
```

2. Ensure you have `model.pkl` (trained model) in the project directory.  
   - If missing, train the model on the **50_Startups dataset** and save using `pickle`.  

3. Run the Flask app:

```bash
python app.py
```

4. Open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## ▶️ Usage

### 1️⃣ Web Interface

- Enter input values into the form on the homepage (`index.html`).  
- The app will return the **predicted profit**.  

### 2️⃣ API Endpoint

Send a POST request with JSON input:

```bash
curl -X POST http://127.0.0.1:5000/predict_api      -H "Content-Type: application/json"      -d '{"R&D Spend": 160000, "Administration": 130000, "Marketing Spend": 300000}'
```

Response:

```json
{
  "prediction": 123456.78
}
```

---

## 📂 Project Structure

```bash
prediction-using-flask/
│
├── app.py              # Flask application
├── model.pkl           # Pickled ML model (Linear Regression)
├── templates/
│   └── index.html      # Frontend template
├── static/             # (Optional) static files (CSS, JS)
├── requirements.txt    # Dependencies
└── README.md           # Project documentation
```

---

## 🤝 Contributing

1. Fork the repository  
2. Create a new branch (`git checkout -b feature-name`)  
3. Commit your changes (`git commit -m "Added new feature"`)  
4. Push to your branch (`git push origin feature-name`)  
5. Open a Pull Request  

---

## 👩‍💻 About

This project is part of my **Machine Learning + Flask deployment practice**.  
The goal is to demonstrate how ML models can be **integrated into real-world web applications**.
