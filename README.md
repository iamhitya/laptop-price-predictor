# 💻 Laptop Price Predictor

A **demo Python application** that predicts laptop prices based on hardware specifications using machine learning. This interactive web app is built with Streamlit and features a modern dark-themed UI for an enhanced user experience.

---

## 🎯 Overview

This application allows users to input laptop specifications and get instant price predictions in Indian Rupees (₹). The prediction model is trained on a comprehensive dataset of laptop specifications and their market prices, utilizing various machine learning techniques to provide accurate price estimates.

---

## ✨ Features

- **Interactive Web Interface**: Clean, modern Streamlit-based UI with dark mode styling
- **Real-time Predictions**: Instant price estimation based on selected specifications
- **Comprehensive Input Options**: 
  - Brand selection (Dell, HP, Lenovo, Apple, etc.)
  - Laptop type (Notebook, Gaming, Ultrabook, etc.)
  - RAM configurations (2GB to 64GB)
  - Storage options (HDD/SSD)
  - Display specifications (size, resolution, touchscreen, IPS)
  - CPU and GPU selection
  - Operating system options
- **Smart Validation**: Built-in checks for missing or invalid inputs
- **Calculated PPI**: Automatically computes pixels per inch from screen size and resolution
- **Price Display**: Results shown in Indian Rupees with formatted output

---

## 🛠️ Tech Stack

### **Core Technologies**
- **Python 3.11.6**: Programming language
- **Streamlit**: Web application framework
- **Scikit-learn**: Machine learning library for model training
- **Pandas & NumPy**: Data manipulation and numerical computing
- **Matplotlib & Seaborn**: Data visualization during model development

### **Deployment**
- **Gunicorn**: WSGI HTTP Server
- **Procfile**: Heroku/cloud deployment configuration

---

## 📦 Installation & Setup

### **Prerequisites**
- Python 3.11.6 or higher
- pip package manager

### **Local Development**

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd laptop-price-predictor
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run app.py
   ```

4. **Access the app**
   - Open your browser and navigate to `http://localhost:8501`

---

## 📁 Project Structure

```
laptop-price-predictor/
│
├── app.py                           # Main Streamlit application
├── laptop_price_prediction.ipynb    # Jupyter notebook with model training
├── laptop_data.csv                  # Dataset for training
├── pipe.pkl                         # Trained ML pipeline (generated)
├── df.pkl                           # Processed dataframe (generated)
├── requirements.txt                 # Python dependencies
├── runtime.txt                      # Python version specification
├── Procfile                         # Deployment configuration
└── README.md                        # Project documentation
```

---

## 🧠 Machine Learning Pipeline

The application uses a pre-trained machine learning model with the following workflow:

1. **Data Preprocessing**:
   - Cleaning and handling missing values
   - Feature extraction from specifications
   - Converting categorical variables to numerical format

2. **Feature Engineering**:
   - Extracting touchscreen and IPS display features from screen resolution
   - Calculating PPI (Pixels Per Inch) from screen dimensions
   - Processing storage configurations (HDD/SSD)
   - RAM and weight normalization

3. **Model Training**:
   - Training on laptop specifications dataset
   - Using scikit-learn pipelines for preprocessing and prediction
   - Logarithmic transformation for price prediction accuracy

4. **Prediction**:
   - Takes 12 input features: Company, Type, RAM, Weight, Touchscreen, IPS, PPI, CPU, HDD, SSD, GPU, OS
   - Returns exponential transformation of predicted log price

---

## 🎮 How to Use

1. **Select Laptop Specifications**:
   - Choose brand from dropdown (Dell, HP, Lenovo, etc.)
   - Select laptop type (Notebook, Gaming, Ultrabook, etc.)
   - Pick RAM size (2GB to 64GB)
   - Enter weight in kilograms
   - Choose display features (touchscreen, IPS)
   - Select screen size and resolution
   - Pick CPU brand (Intel Core i5, AMD, etc.)
   - Choose GPU brand (Intel, Nvidia, AMD)
   - Select operating system
   - Specify storage (HDD and/or SSD)

2. **Get Prediction**:
   - Click the "🚀 Predict Price" button
   - View the estimated price in Indian Rupees (₹)

3. **Validation**:
   - App validates that all fields are filled
   - Ensures either HDD or SSD (or both) is specified
   - Displays error messages for invalid inputs

---

## 📊 Model Features

The prediction model considers these key features:
- **Brand**: Company/manufacturer
- **Type**: Laptop category (Gaming, Notebook, etc.)
- **RAM**: Memory size in GB
- **Weight**: Physical weight in kg
- **Touchscreen**: Boolean (Yes/No)
- **IPS Display**: Boolean (Yes/No)
- **PPI**: Calculated pixels per inch
- **CPU**: Processor brand
- **HDD**: Hard disk drive storage (GB)
- **SSD**: Solid state drive storage (GB)
- **GPU**: Graphics card brand
- **OS**: Operating system

---

## 🚀 Deployment

### **Heroku Deployment**

The application is configured for Heroku deployment:

1. The `Procfile` specifies the web server command
2. The `runtime.txt` defines the Python version
3. Deploy using Heroku CLI:
   ```bash
   heroku create your-app-name
   git push heroku main
   heroku open
   ```

### **Other Platforms**

Can be deployed on:
- **Streamlit Cloud**: Direct deployment from GitHub
- **AWS**: Using EC2 or Elastic Beanstalk
- **Google Cloud**: Using App Engine or Cloud Run
- **Azure**: Using Web Apps

---

## 📝 Requirements

```txt
pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  
streamlit  
gunicorn
```

---

## 🎨 UI Features

- **Dark Mode Theme**: Modern gradient background
- **Responsive Design**: Two-column layout for better organization
- **Custom Styling**: CSS-enhanced buttons and result displays
- **Input Validation**: Real-time error alerts
- **Visual Feedback**: Hover effects and smooth transitions

---

## 🤝 Contributing

This is a demo application. Feel free to fork, modify, and enhance it for your own use cases.

---

## 📄 License

This is a demonstration project for educational and portfolio purposes.

---

## 👨‍💻 Author

Built as a demo Python application showcasing machine learning integration with web interfaces.

---

## 📧 Contact

For questions or feedback about this demo application, please reach out through the repository's issue tracker.

---

**Note**: This is a demonstration application. The prediction model is trained on sample data and should be used for educational purposes only. Actual laptop prices may vary based on market conditions, location, and other factors.