# AgriBuddy - AI-Powered Agriculture Assistant

A machine learning and deep learning-powered web application that provides intelligent recommendations for crop selection, fertilizer usage, and plant disease detection. Built with Flask and modern web technologies for a seamless user experience.

## 🌾 Features

- **Crop Recommendation**: Get personalized crop recommendations based on soil characteristics and climate conditions
- **Fertilizer Recommendation**: Receive tailored fertilizer suggestions to optimize crop yield
- **Disease Detection**: Upload plant images to detect and identify diseases with deep learning models
- **Modern UI**: Responsive, intuitive interface built with Bootstrap 5
- **Real-time Predictions**: Instant ML-powered predictions from trained models

## 🛠️ Tech Stack

### Backend
- **Framework**: Flask 2.0.3
- **ML/DL**: PyTorch 1.12.1, torchvision 0.13.1
- **Data Processing**: pandas 1.3.5, numpy 1.21.6
- **ML Models**: scikit-learn 1.0.2

### Frontend
- **CSS Framework**: Bootstrap 5.3.0
- **Typography**: Google Fonts (Poppins, Playfair Display)
- **Icons**: Font Awesome 6.4.0
- **Styling**: Custom CSS with modern gradients and animations

### Environment
- **Python**: 3.10
- **Package Manager**: pip
- **Virtual Environment**: venv

## 📋 Prerequisites

- Python 3.10 or higher
- pip package manager
- Virtual environment (recommended)

## 🚀 Setup & Installation

### 1. Clone the Repository
```bash
git clone <repository-url>
cd agro.ai-main
```

### 2. Create Virtual Environment
```bash
python -m venv .venv
```

### 3. Activate Virtual Environment

**Windows (PowerShell):**
```bash
.\.venv\Scripts\Activate.ps1
```

**Windows (CMD):**
```bash
.\.venv\Scripts\activate.bat
```

**macOS/Linux:**
```bash
source .venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Run the Application
```bash
python app.py
```

The application will start on `http://localhost:5000`

## 📁 Project Structure

```
agro.ai-main/
├── app.py                      # Main Flask application
├── config.py                   # Configuration settings
├── model.py                    # ML model utilities
├── disease_dic.py              # Disease classification dictionary
├── fertilizer_dic.py           # Fertilizer recommendation dictionary
├── requirements.txt            # Python dependencies
├── README.md                   # This file
│
├── Data/                       # Training & reference data
│   ├── FertilizerData.csv
│   └── Final_Data_recomm.csv
│
├── Trained_Model/             # Pre-trained models
│   └── plant_disease_model.pth
│
├── static/                     # Static assets
│   ├── css/
│   │   ├── bootstrap.css
│   │   ├── style.css
│   │   └── font-awesome.min.css
│   ├── images/
│   └── scripts/
│       └── cities.js
│
└── templates/                  # HTML templates
    ├── layout.html             # Base template
    ├── index.html              # Home page
    ├── crop.html               # Crop recommendation page
    ├── crop-result.html        # Crop results
    ├── fertilizer.html         # Fertilizer recommendation page
    ├── fertilizer-result.html  # Fertilizer results
    ├── disease.html            # Disease detection page
    ├── disease-result.html     # Disease results
    ├── login.html              # Login page
    ├── signup.html             # Sign up page
    └── try_again.html          # Error recovery page
```

## 🔍 API Endpoints

### Main Routes
- `GET /` - Home page
- `GET /crop-recommend` - Crop recommendation form
- `POST /crop-predict` - Get crop recommendation
- `GET /fertilizer` - Fertilizer recommendation form
- `POST /fertilizer-predict` - Get fertilizer recommendation
- `GET /disease` - Disease detection form
- `POST /disease-predict` - Detect plant disease

## 🧠 Machine Learning Models

### Crop Recommendation
- **Input**: Soil nitrogen, phosphorus, potassium levels, temperature, humidity, pH, rainfall
- **Output**: Best crop to plant in given conditions
- **Algorithm**: Based on historical agricultural data and climate patterns

### Fertilizer Recommendation
- **Input**: Crop type, soil nitrogen, phosphorus, potassium levels
- **Output**: Recommended fertilizer with dosage
- **Data Source**: FertilizerData.csv

### Disease Detection
- **Input**: Plant leaf image
- **Output**: Disease classification and confidence score
- **Model**: Deep learning CNN (plant_disease_model.pth)
- **Framework**: PyTorch

## 📊 Data Sources

- **Crop & Fertilizer Data**: `Data/FertilizerData.csv` and `Data/Final_Data_recomm.csv`
- **Pre-trained Model**: `Trained_Model/plant_disease_model.pth`

## ⚙️ Configuration

Edit `config.py` to customize:
- Flask settings
- Model paths
- Application parameters
- Upload directories

## 🐛 Troubleshooting

### Port Already in Use
If port 5000 is already in use, modify the port in `app.py`:
```python
if __name__ == '__main__':
    app.run(debug=True, port=5001)  # Change to desired port
```

### Model Loading Issues
Ensure the trained model is present at `Trained_Model/plant_disease_model.pth` and PyTorch is properly installed:
```bash
pip install torch torchvision
```

### Import Errors
Make sure all dependencies are installed:
```bash
pip install -r requirements.txt
```

## 📝 License

This project is open source. Please check the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bug reports and feature requests.

## 📧 Support

For issues, questions, or suggestions, please open an issue in the repository.

---

**Note**: This is a local development version. All features are available on localhost. For production deployment, additional configuration may be required.

