# Chronic Kidney Disease Prediction

This project is designed to predict the likelihood of a patient having Chronic Kidney Disease (CKD) based on various medical attributes. The project is built using a machine learning model trained with patient data and a web interface to input new patient data and view the prediction results.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Training](#model-training)
- [Web Interface](#web-interface)
- [Dependencies](#dependencies)
- [License](#license)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/ckd-prediction.git
   cd ckd-prediction
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Ensure you have the `kidney.pkl` file in the `models` directory:**
   Make sure the pre-trained model file (`kidney.pkl`) is in the `models` directory within the project.

## Usage

1. **Run the Flask application:**
   ```bash
   python app.py
   ```

2. **Open your browser and go to:**
   ```
   http://127.0.0.1:5000
   ```

3. **Use the web interface to input patient data and predict CKD:**
   - Fill in the required fields on the home page.
   - Click the "Predict" button to get the prediction result.

## Project Structure

- `app.py`: The main Flask application file that sets up the web server and routes.
- `models/kidney.pkl`: The pre-trained machine learning model for predicting CKD.
- `templates/main.html`: The base HTML template for the web pages.
- `templates/home.html`: The HTML template for the home page where users input patient data.
- `templates/predict.html`: The HTML template for displaying the prediction results.
- `kidney.ipynb`: Jupyter notebook containing the code for training the machine learning model.
- `static/`: Directory containing static files such as images and CSS.
- `requirements.txt`: File listing the dependencies needed for the project.

## Model Training

The machine learning model was trained using a dataset of patient medical records with the following attributes:
- Age
- Blood Pressure
- Specific Gravity
- Albumin
- Sugar
- Red Blood Cells
- Pus Cell
- Pus Cell Clumps
- Bacteria
- Blood Glucose Random
- Blood Urea
- Serum Creatinine
- Sodium
- Potassium
- Haemoglobin
- Packed Cell Volume
- White Blood Cell Count
- Red Blood Cell Count
- Hypertension
- Diabetes Mellitus
- Coronary Artery Disease
- Appetite
- Pedal Edema
- Anemia

The training process and model evaluation can be found in the `kidney.ipynb` notebook.

## Web Interface

The web interface is built using Flask and Bootstrap. The home page (`home.html`) contains a form where users can input patient data. Upon submission, the data is sent to the server, and the prediction result is displayed on the `predict.html` page.

### Additional CSS and Animations

Custom CSS is used to style the web pages. Additional animations can be added using CSS or JavaScript as needed. The `predict.html` page displays the prediction result with appropriate alert styles for positive and negative predictions.

## Dependencies

- Flask==2.1.2
- numpy==1.23.0
- Pillow==9.1.1


Install the dependencies using:
```bash
pip install -r requirements.txt
```
