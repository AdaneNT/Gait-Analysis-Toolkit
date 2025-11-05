
# Gait Analysis Toolkit
Applications include remote monitoring of Parkinson’s disease, stroke rehabilitation, and activity tracking in healthcare and smart environments. A machine learning-based gait analysis system using wearable inertial sensors to recognize common human activities of daily living (ADLs), such as:
- 🚶 Walking
- 🏃 Jogging
- 🧍 Standing
- 🪑 Sitting
- ⬆️ Going Upstairs
- ⬇️ Going Downstairs

This project demonstrates the real-world deployment of an ML model via a RESTful API built with Flask, served through Docker, and documented using Swagger UI. More descriptions about the toolkit can be accessed from the [project website here](https://alameda.catalink.eu/ga_ntnu.html). 

---

## Tech Stack

- **Python**
- **ML Algorithm**
- **Scikit-learn**
- **Flask (REST API)**
- **Swagger UI**
- **Docker**
- **Inertial Sensor Dataset** (Smartphone-based)

---
## Project Structure
```text
.
├── classifier_rf.pkl         # Pre-trained Random Forest classifier
├── gait_api.py               # Flask server with REST endpoints
├── requirements.txt          # Dependencies
├── Dockerfile                # Docker image setup
├── X_test_raw.txt            # Example test input
└── README.md                 # Project documentation           
```
## Installation Instructions
The GA toolkit has been packaged in a Dockerized container. The toolkit’s image can be tested and run on a local machine:
### Option 1: Run Docker Image from Docker Hub

```bash
# Step 1: Pull the Docker image
docker pull adanentnu/gait_module

# Step 2: Run the container
docker run -p 8088:8080 adanentnu/gait_module

# Step 3: Open your browser
http://localhost:8088/apidocs
```
## Option 2: Build and Run Locally
## Clone the repository
git clone [https://github.com/adanent/Gait-Analysis-Toolkit](https://github.com/AdaneNT/Gait-Analysis-Toolkit)-.git

cd Gait-Analysis-Toolkit-

## Build Docker image
docker build -t gait_module .

## Run container
docker run -p 8082:8080 gait_module

## Demo
Visit the Swagger UI on your local host:
http://localhost:8088/apidocs

Use X_test_raw.txt to test the API endpoint /predict.

## Dataset Information
###  Smart Belt Dataset(Custom-Collected)
This toolkit uses a pre-trained model trained on a custom smartphone-based dataset collected from wearable inertial sensors (IMUs):
- We collected from 12 participants using a custom belt with 3 IMU sensors (sampling rate: 100 Hz)
- Activities: Walking, walking upstairs/downstairs, sitting, standing, lying
- Annotated using [**NOVA**](https://github.com/hcmlab/nova)
- Dataset available in the [`Datasets/`](./Datasets/) folder (`smart_belt_dataset.csv`)  
  or [external link](https://alamedaproject.eu/)
- Oversampling applied to balance activity classes



