# Network Anomaly Detection
![Python version](https://img.shields.io/badge/python-3.10+-blue)
![GitHub Actions](https://github.com/webpro255/network-anomaly-detection/actions/workflows/python-app.yml/badge.svg)
![GitHub last commit](https://img.shields.io/github/last-commit/webpro255/network-anomaly-detection)
![GitHub issues](https://img.shields.io/github/issues/webpro255/network-anomaly-detection)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/webpro255/network-anomaly-detection/blob/main/LICENSE)
![GitHub contributors](https://img.shields.io/github/contributors/webpro255/network-anomaly-detection)

Welcome to the Network Anomaly Detection project! This repository showcases a practical application of machine learning in cybersecurity by monitoring and detecting unusual activities in a network. 

## Features
- **Real-time Anomaly Detection**: Monitors network traffic and identifies anomalies in real-time using machine learning.
- **REST API**: Provides a RESTful API for easy integration and real-time anomaly detection.
- **Extensible Design**: Easily adaptable to different network environments and customizable for various use cases.

## Tools and Technologies
- **Python**: The core programming language used in the project.
- **Flask**: A micro web framework for building the REST API.
- **Scikit-learn**: For training the anomaly detection model.
- **Pandas**: For data manipulation and preprocessing.
- **Joblib**: For saving and loading machine learning models.
- **Wireshark/tcpdump**: For capturing network traffic data.

## Use Cases
### Home Network Monitoring
Monitor and analyze traffic in your home network to detect unusual activities, such as unauthorized access attempts or unusual data transfers.

### Small Business Network Security
Deploy in a small business environment to enhance network security by identifying potential threats and anomalies in network traffic.

### Educational Tool
Serve as an educational tool for students and professionals learning about network security and machine learning applications in cybersecurity.

## Getting Started

### 1. Clone the Repository
```sh
git clone https://github.com/webpro255/network-anomaly-detection.git
cd network-anomaly-detection
```
### 2. Install Dependencies

Ensure you have Python 3.10+ installed, then install the necessary Python packages:
```sh
pip install -r requirements.txt
```
### 3. Run the Flask Application

Start the Flask application to serve the REST API:
```sh
python3 app.py
```
### 4. Test the Application

Use the following curl command to test the API with sample data:
```sh
curl -X POST http://<your-server-ip>:5000/predict -H "Content-Type: application/json" -d '[{"src_ip": "192.168.0.1", "dest_ip": "192.168.0.2", "src_port": 1234, "dest_port": 80, "protocol": "TCP", "packet_size": 100}]'
```
### API Endpoints
`/`
Returns a welcome message for the application.
`/predict`
Accepts JSON data representing network traffic and returns a prediction of anomalies. Expects data in the following format:
```json
[
    {
        "src_ip": "192.168.0.1",
        "dest_ip": "192.168.0.2",
        "src_port": 1234,
        "dest_port": 80,
        "protocol": "TCP",
        "packet_size": 100
    }
]
```
### Project Structure
- **app.py**: The main Flask application file.
- **anomaly_detection.py**: Contains the anomaly detection logic.
- **requirements.txt**: Python dependencies.
- **kddcup.data_10_percent**: Sample network traffic data (for training and testing).
- **pipeline.pkl**: Serialized machine learning model.
- **templates**: HTML templates for the web interface.

### Future Improvements
- **Integration with Real-time Traffic Capture**: Use Wireshark or tcpdump for real-time traffic capture.
- **Dashboard**: Develop a real-time dashboard for monitoring network traffic and visualizing anomalies.
- **Enhanced Model**: Improve the anomaly detection model using more advanced machine learning techniques.

### Contributing
We welcome contributions! Please read our contributing guidelines before making any changes.

