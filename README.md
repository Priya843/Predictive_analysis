# Predictive Analysis for Manufacturing Operations

This repository contains the implementation of a predictive analysis model for manufacturing operations. The project includes a RESTful API to predict machine downtime or production defects using manufacturing data.

---

## **Project Overview**

The objective of this project is to:
1. Build a predictive analysis model for manufacturing operations.
2. Provide RESTful API endpoints to upload data, train the model, and make predictions.

The API uses a simple supervised machine learning model (Logistic Regression or Decision Tree) and is implemented using Flask.

---

## **Endpoints**

### **1. Predict Machine Downtime**
- **Endpoint**: `/predict`
- **Method**: POST
- **Description**: Predict downtime based on input features.
- **Input**:
  ```json
  {
    "Temperature": 85,
    "Run_Time": 150
  }
  ```
- **Example Response**:
  ```json
  {
    "Downtime": "Yes",
    "Confidence": 0.87
  }
  ```

---

## **Setup Instructions**

### **1. Clone the Repository**
Clone the repository to your local machine:
```bash
git clone https://github.com/<your-username>/predictive_analysis.git
cd predictive_analysis
```

### **2. Install Dependencies**
Install the required Python libraries using:
```bash
pip install -r requirement.txt
```

### **3. Run the Application**
Run the `app.py` script to start the Flask server:
```bash
python app.py
```

The API will be available at `http://127.0.0.1:5000`.

---

## **File Structure**

```
prediction/
│
├── app.py                     # Main Python script for predictions
├── models/
│   └── model.pkl              # Pretrained model file
├── data/
│   └── balanced_manufacturing_data.csv  # Dataset file
├── Report.pdf                 # Project report
└── requirement.txt            # Python dependencies
```

---

## **Dataset**

### **Dataset Columns**
The dataset contains the following columns:
- `Machine_ID`: Unique identifier for each machine.
- `Temperature`: Operating temperature (in degrees).
- `Run_Time`: Machine runtime in minutes.
- `Downtime_Flag`: Binary flag (1 for downtime, 0 for no downtime).

### **Example Row**
```csv
Machine_ID,Temperature,Run_Time,Downtime_Flag
1,75,120,0
```

---

## **Testing the API**

### **Using Postman**
1. **Predict Downtime**:
   - Method: `POST`
   - URL: `http://127.0.0.1:5000/predict`
   - Body: Raw JSON:
     ```json
     {
       "Temperature": 85,
       "Run_Time": 150
     }
     ```

---

## **Report**
The full project report is included in this repository as `Report.pdf`.

---

## **Author**
Developed by **[Your Name]**.

---

## **License**
This project is licensed under the MIT License.
