# Job Recommendation System Using Resume Parsing

A comprehensive machine learning-based web application that automates resume screening, categorizes resumes, and provides intelligent job recommendations using Natural Language Processing (NLP) techniques.

## Features

- **Resume Parsing**: Extracts essential information from PDF and TXT resumes including:
  - Contact details (phone, email)
  - Skills and technologies
  - Educational background
  - Work experience
- **Resume Categorization**: Automatically categorizes resumes using Random Forest classifier
- **Job Recommendations**: Provides top 3 job recommendations using XGBoost algorithm
- **Web Interface**: User-friendly Flask web application for easy resume upload and analysis
- **Multi-format Support**: Supports both PDF and TXT file formats

## Technology Stack

- **Backend**: Python, Flask
- **Machine Learning**: 
  - scikit-learn (Random Forest Classifier)
  - XGBoost (Job Recommendation)
  - TF-IDF Vectorization
- **PDF Processing**: PyPDF2
- **Frontend**: HTML, CSS, JavaScript
- **Data Processing**: NumPy, Pandas
- **Visualization**: Matplotlib, Seaborn

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Bhanuraj23m0316iitb/Job-Recommendation-System-using-Resume-Parsing.git
   cd Job-Recommendation-System-using-Resume-Parsing
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv resume_env
   # On Windows
   resume_env\Scripts\activate
   # On macOS/Linux
   source resume_env/bin/activate
   ```

3. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Verify model files**
   Ensure the following model files are present in the `Models/` directory:
   - `rf_classifier_categorization.pkl`
   - `tfidf_vectorizer_categorization.pkl`
   - `xgb_classifier_job_recommendation.pkl`
   - `tfidf_vectorizer_job_recommendation.pkl`
   - `label_encoder_job_recommendation.pkl`

## Running the Application

1. **Start the Flask application**
   ```bash
   python app.py
   ```

2. **Access the web interface**
   Open your web browser and navigate to:
   ```
   http://localhost:5000
   ```

3. **Upload and analyze resumes**
   - Click on "Choose File" to select a PDF or TXT resume
   - Click "Predict" to process the resume
   - View the results including category prediction, job recommendations, and extracted information

## Project Structure

```
Job-Recommendation-System-using-Resume-Parsing/
├── app.py                                    # Main Flask application
├── requirements.txt                          # Python dependencies
├── README.md                                # Project documentation
├── .gitignore                               # Git ignore file
├── Models/                                  # Pre-trained ML models
│   ├── rf_classifier_categorization.pkl
│   ├── tfidf_vectorizer_categorization.pkl
│   ├── xgb_classifier_job_recommendation.pkl
│   ├── tfidf_vectorizer_job_recommendation.pkl
│   └── label_encoder_job_recommendation.pkl
├── templates/                               # HTML templates
│   └── index.html                          # Main web interface
├── Sample data/                            # Sample resume files for testing
│   ├── advocate.txt
│   ├── banking.txt
│   ├── designer.pdf
│   ├── Healthcare.txt
│   ├── info resume.pdf
│   └── Teacher.pdf
├── Resume Catogorization prediction.ipynb  # Model training notebook
├── Resume Job Recommendation System.ipynb  # Job recommendation notebook
└── Extracted Info and hiring process.ipynb # Information extraction notebook
```

## Testing the Application

Use the sample resume files in the `Sample data/` directory to test the application:

1. Upload any of the sample files (PDF or TXT format)
2. Click "Predict" to see the analysis results
3. Review the extracted information, category prediction, and job recommendations

## How It Works

1. **Resume Upload**: Users upload PDF or TXT resume files through the web interface
2. **Text Extraction**: The system extracts text content from uploaded files
3. **Text Preprocessing**: Cleans and preprocesses the extracted text
4. **Information Extraction**: Uses regex patterns to extract:
   - Contact information (phone, email)
   - Skills from a predefined skill database
   - Educational qualifications
5. **Categorization**: Uses TF-IDF vectorization and Random Forest to categorize resumes
6. **Job Recommendation**: Employs XGBoost classifier to recommend top 3 suitable job roles
7. **Results Display**: Shows all extracted information and predictions on the web interface

## Use Cases

- **Recruitment Agencies**: Automate initial resume screening process
- **HR Departments**: Quickly categorize and match candidates to job openings
- **Job Seekers**: Get insights into resume content and suitable job recommendations
- **Career Counselors**: Analyze candidate profiles for career guidance

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## License

This project is available for educational and research purposes.

## Acknowledgments

- Machine learning models trained on resume datasets
- Flask framework for web application development
- scikit-learn and XGBoost for machine learning algorithms




