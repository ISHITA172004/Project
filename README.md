Birth Weight Prediction API
A Flask-based REST API that predicts a baby's birth weight based on various maternal health factors. This project uses Flask-RESTX for API documentation (Swagger UI), integrates a pre-trained Machine Learning model, and includes automated testing with pytest.

🚀 Features
✅ Predicts baby birth weight using maternal data
✅ Swagger UI documentation (/docs endpoint)
✅ REST API with multiple namespaces (Hello, User, Prediction)
✅ Includes automated test cases with pytest
✅ Model loading using pickle
✅ JSON-based request & response format

🛠 Tech Stack
Backend: Flask, Flask-RESTX

ML Model: Scikit-learn (loaded via pickle)

Testing: pytest

Data Handling: Pandas, NumPy

Deployment Ready: Configured for Gunicorn (Render/Heroku)

📂 Project Structure
bash
Copy code
├── app.py              # Main Flask app with API routes  
├── test_app.py          # Unit tests using pytest  
├── model.pkl            # Pre-trained ML model (binary file)  
├── requirements.txt      # Python dependencies  
└── README.md             # Project documentation  
⚙️ Setup Instructions
1️⃣ Create a virtual environment

python -m venv venv  
source venv/bin/activate      # On Linux/Mac  
venv\Scripts\activate         # On Windows  
2️⃣ Install dependencies

pip install -r requirements.txt  
3️⃣ Run the Flask server

python app.py  
Your API will now run locally at:
👉 http://127.0.0.1:5000/

Swagger UI will be available at:
👉 http://127.0.0.1:5000/docs

🔥 API Endpoints
🟢 Hello API
GET /hello
Response:

json
Copy code
{
  "msg": "Hello World!"
}
🟢 Prediction API
POST /predict

Request Body (JSON):

json
Copy code
{
  "gestation": [279],
  "parity": [0],
  "age": [27],
  "height": [70],
  "weight": [100],
  "smoke": [0]
}
Response:

json
Copy code
{
  "Prediction": 123.45
}
🧪 Running Tests
Run unit tests using pytest:

bash
Copy code
pytest test_app.py  
🚀 Deployment
Designed for Render/Heroku using Gunicorn.

Start command:

gunicorn app:app  
🤝 Contribute
Feel free to fork this repo, make improvements, and submit a pull request!
