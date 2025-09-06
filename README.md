# Smart VTU Marks & CGPA Predictor

A comprehensive web-based application for VTU students to calculate SGPA/CGPA, predict required internal marks, and track academic progress across semesters.

## 🎯 Features

### 1. SGPA/CGPA Calculator
- Calculate semester and cumulative GPA based on VTU marking schemes
- Support for multiple schemes (2018, 2021, 2022)
- Subject-wise breakdown with grade analysis
- Real-time calculation with visual feedback

### 2. Internal Marks Predictor
- Predict minimum required marks in remaining internals
- Set target grades (S, A, B, C, D)
- Subject-wise recommendations
- Study tips and guidance

### 3. Progress & Reports
- Track academic progress across semesters
- Interactive charts and graphs
- CGPA trends and analysis
- Semester-wise performance breakdown

## 🛠️ Tech Stack

### Backend
- **Flask** - Python web framework
- **SQLite** - Database for storing schemes, subjects, and results
- **Flask-CORS** - Cross-origin resource sharing

### Frontend
- **React.js** - User interface library
- **Tailwind CSS** - Utility-first CSS framework
- **Chart.js** - Data visualization
- **Axios** - HTTP client for API calls

## 📁 Project Structure

```
vtu_marks_predictor/
├── backend/
│   ├── app.py                 # Flask application
│   └── requirements.txt       # Python dependencies
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/        # React components
│   │   │   ├── Dashboard.js
│   │   │   ├── Calculator.js
│   │   │   ├── Predictor.js
│   │   │   ├── Progress.js
│   │   │   ├── SchemeSelector.js
│   │   │   ├── SubjectMarksForm.js
│   │   │   ├── ResultsDisplay.js
│   │   │   ├── PredictionForm.js
│   │   │   ├── PredictionResults.js
│   │   │   └── ProgressForm.js
│   │   ├── App.js
│   │   ├── index.js
│   │   └── index.css
│   ├── package.json
│   ├── tailwind.config.js
│   └── postcss.config.js
└── README.md
```

## 🚀 Installation & Setup

### Prerequisites
- Python 3.7+
- Node.js 14+
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
```bash
cd vtu_marks_predictor/backend
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the Flask application:
```bash
python app.py
```

The backend will be available at `http://localhost:5000`

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd vtu_marks_predictor/frontend
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The frontend will be available at `http://localhost:3000`

## 📊 API Endpoints

### Schemes
- `GET /api/schemes` - Get all available VTU schemes

### Subjects
- `GET /api/subjects/{scheme_id}/{semester}` - Get subjects for a scheme and semester

### Calculations
- `POST /api/calculate-sgpa` - Calculate SGPA for given marks and credits
- `POST /api/calculate-cgpa` - Calculate CGPA from multiple semesters
- `POST /api/predict-internal` - Predict required internal marks for target grade

### Student Data
- `POST /api/save-results` - Save student results
- `GET /api/student-progress/{student_id}` - Get student progress data

## 🎨 Features in Detail

### VTU Scheme Support
- **Scheme 2018**: 3 internals of 25 marks each
- **Scheme 2021**: 2 internals of 50 marks each  
- **Scheme 2022**: 3 internals of 25 marks each + assignments

### Grade Calculation
- **S Grade**: 90-100 marks (10 points)
- **A Grade**: 80-89 marks (9 points)
- **B Grade**: 70-79 marks (8 points)
- **C Grade**: 60-69 marks (7 points)
- **D Grade**: 50-59 marks (6 points)
- **E Grade**: 45-49 marks (5 points)
- **F Grade**: Below 45 marks (0 points)

### SGPA Calculation
```
SGPA = Σ(Grade Points × Credits) / Σ(Credits)
```

### CGPA Calculation
```
CGPA = Σ(SGPA × Credits) / Σ(Credits)
```

## 🔧 Usage

### 1. SGPA Calculator
1. Select your VTU scheme
2. Choose the semester
3. Enter marks for each subject
4. Click "Calculate SGPA" to get results

### 2. Internal Predictor
1. Select scheme and semester
2. Set your target grade
3. Enter completed internal marks
4. Get predictions for required marks in remaining internals

### 3. Progress Tracking
1. Enter your student ID
2. View semester-wise progress
3. Analyze CGPA trends
4. Add new results as you complete semesters

## 🎯 Benefits

- **Accuracy**: Precise calculations based on VTU marking schemes
- **Transparency**: Clear breakdown of grades and calculations
- **Motivation**: Goal-setting and progress tracking
- **Planning**: Strategic study planning with predictions
- **Accessibility**: Web-based, works on any device

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

This project is open source and available under the MIT License.

## 🆘 Support

For issues and questions:
1. Check the documentation
2. Search existing issues
3. Create a new issue with detailed description

## 🔮 Future Enhancements

- [ ] Support for more VTU schemes
- [ ] Mobile app version
- [ ] Export results to PDF
- [ ] Integration with college systems
- [ ] Advanced analytics and insights
- [ ] Study plan recommendations
- [ ] Peer comparison features

---

**Built with ❤️ for VTU students**
