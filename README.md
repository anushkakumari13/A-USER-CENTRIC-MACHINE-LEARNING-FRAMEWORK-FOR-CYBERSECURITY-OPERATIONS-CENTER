# A-USER-CENTRIC-MACHINE-LEARNING-FRAMEWORK-FOR-CYBERSECURITY-OPERATIONS-CENTER

A machine learning-based cyber threat detection system that empowers SOC analysts to identify and prioritize risky users using automated risk scoring based on SIEM alert data.

## Overview

This project proposes a **User-Centric Machine Learning Framework** to assist Security Operations Center (SOC) teams in handling high volumes of alerts by intelligently prioritizing users based on risk. The framework uses event log data, SIEM alerts, and ML models to improve threat detection and reduce false positives.

## Purpose

Traditional SOC systems suffer from:

- High false positive rates in SIEM alerts
- Manual, time-consuming alert investigations
- Limited scalability with increasing data

**Our solution**: An ML-based framework that provides a **risk score** for each user, helping SOC analysts focus on high-risk individuals and enhance cybersecurity efficiency.

## Key Features

- **User Risk Scoring**: Uses SVM to classify user behavior as high or low risk.
- **SIEM Alert Processing**: Integrates various logs including DNS, DHCP, IDS/IPS.
- **Data Preprocessing**: Cleans and transforms data for better model accuracy.
- **Web Interface (Django)**: Admin and user dashboards for transactions, alerts, and risk analysis.
- **Graphical Analysis**: Visualizes user risk and threat patterns using charts.

## Tech Stack

| Layer         | Technology              |
|--------------|--------------------------|
| Language      | Python 3.7               |
| Backend       | Django                   |
| Frontend      | HTML, CSS, JS            |
| Database      | MySQL                    |
| ML Libraries  | Scikit-learn, Pandas, NumPy, Matplotlib |
| Deployment    | XAMPP                    |

##  Setup Instructions

### Prerequisites

Install the following Python libraries:

```bash
pip install numpy pandas scikit-learn matplotlib opencv-python django
```

### Setup Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/user-centric-cybersec-ml.git
   cd user-centric-cybersec-ml
   ```

2. **Configure MySQL database**:
   - Update `settings.py` in the Django project with your database credentials.
   - Run migrations:
     ```bash
     python manage.py makemigrations
     python manage.py migrate
     ```

3. **Run the Django server**:
   ```bash
   python manage.py runserver
   ```

4. **Open in browser**:
   ```
   http://127.0.0.1:8000/
   ```

## Project Structure

```
├── ML/
│   ├── svm_model.pkl
│   ├── preprocessing.py
│   └── train_model.py
├── cybersec_app/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── templates/
│   └── static/
├── db.sqlite3
├── manage.py
└── README.md
```

## ML Model - SVM (Support Vector Machine)

The project uses SVM for binary classification of risky vs non-risky users:

- Preprocessing includes cleaning, labeling, and scaling alert data.
- Trained model stored as `svm_model.pkl`.
- Accuracy metrics are used for evaluation.


## Future Enhancements

- Integration with live SIEM tools (e.g. Splunk, Elastic Stack).
- Support for deep learning (LSTM/CNN) for anomaly detection.
- Real-time alerting system using WebSockets.
- Multi-level user privilege and API integration.

## License

This project is licensed under the **MIT License**.

