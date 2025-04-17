# ML Deployment Project (Exercise 5)

This repository contains materials for the MLOps Course(CPE393) **Exercise 5** which focusing on deploying machine learning models as APIs. However, the Exercise 1-4 https://github.com/KwinyarutP/mldeployment-cpe393-MLOps1-4.git

## Overview

This project demonstrates how to create, package and deploy machine learning models as REST APIs. It covers the entire MLOps workflow from model training to deployment and testing. 

## 📁 Repository Structure

- `modeltrain.py`: Script for training the model and exporting it as `housing_price_model.pkl`.
- `Housing.csv`: Dataset used for training the model.
- `app/`: Contains the FastAPI application to serve the trained model.
- `Dockerfile`: Defines how the Docker image is built.
- `Exercise 5: Dockerize Your Own Model.png`: Screenshot demonstrating the Dockerized model in Exercise 5.

## API Screenshots

The `Exercise 5: Dockerize Your Own Model` picture contains screenshots demonstrating successful API requests and responses in Exercise 5. These images provide visual verification that the API is functioning correctly with test case.

## Setup and Installation

1. Clone the repository:
   ```
   git clone https://github.com/KwinyarutP/house_prediction-MLOps5.git
   
   cd house_prediction-MLOps5
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Training the Model

To train the model and generate the `housing_price_model.pkl` file:

```
python modeltrain.py
```

## Running the API

### With Docker

Build the Docker image:
```
docker build -t ml-deployment .
```

Run the container:
```
docker run -p 9000:9000 ml-deployment
```

## API Usage

Once the API is running, you can access the interactive Swagger UI documentation at `http://localhost:9000/predict`.