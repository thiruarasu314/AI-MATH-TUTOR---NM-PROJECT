# AI-MATH-TUTOR---NM-PROJECT
# AI Math Tutor — Image-Based Algebra Solver

AI Math Tutor is a Python-based application that solves algebra problems from images.
Users can upload a picture of a math equation, and the system automatically detects the equation using OCR, converts it to a mathematical expression, and provides step-by-step solutions.

---

## Features

* Upload or capture an image of a math equation
* Automatic OCR-based equation detection
* Converts detected math expressions to LaTeX
* Solves algebra equations using SymPy
* Displays step-by-step solution explanations
* Detects possible mistakes in the equation
* Simple web interface using Streamlit

---

## Technology Stack

* **Python**
* **Streamlit** – Web interface
* **OpenCV (cv2)** – Image preprocessing
* **Tesseract OCR** – Text recognition
* **SymPy** – Symbolic mathematics solver
* **Pillow** – Image processing
* **NumPy** – Numerical operations

---

## Project Structure

```
ai_math_tutor/
│
├── app.py                 # Streamlit web application
├── sample_generator.py    # Script to generate sample equation images
├── smoke_test.py          # Pipeline testing script
├── run_smoke_test.py      # Quick system test
├── requirements.txt       # Required Python libraries
│
├── utils/
│   └── image_utils.py     # Image preprocessing utilities
│
├── vision/
│   └── ocr.py             # OCR extraction logic
│
├── solver/
│   └── equation_solver.py # Equation parsing and solving
│
├── checker/
│   └── mistake_checker.py # Detects possible mistakes
│
├── prompts/               # Prompt templates for LLM conversion
├── samples/               # Sample images for testing
└── README.md
```

---

## Installation

### 1. Clone the Repository

```
git clone https://github.com/yourusername/ai-math-tutor.git
cd ai-math-tutor
```

### 2. Install Dependencies

```
pip install -r requirements.txt
```

### 3. Install Tesseract OCR

Download from:

https://github.com/UB-Mannheim/tesseract/wiki

Add Tesseract to your system PATH.

---

## Running the Application

Start the Streamlit app:

```
streamlit run app.py
```

Then open the browser at:

```
http://localhost:8501
```

---

## Generating Sample Images

To generate example algebra problem images:

```
python sample_generator.py
```

Images will be created in the `samples/` folder.

---

## Running Smoke Tests

To test the full pipeline:

```
python run_smoke_test.py
```

This will:

1. Generate sample images
2. Run OCR detection
3. Convert expressions
4. Solve equations

---

## Example Workflow

1. Upload an image containing an algebra equation.
2. The system preprocesses the image.
3. OCR extracts the math expression.
4. The equation is parsed and solved using SymPy.
5. Step-by-step solutions are displayed in the interface.

---

## Optional AI Integration

The system can optionally use LLMs for improved LaTeX conversion.

Environment variables:

```
OPENAI_API_KEY=your_openai_key
GEMINI_API_KEY=your_gemini_key
```

---

## Future Improvements

* Handwritten math recognition
* Support for calculus problems
* Graph plotting for equations
* Improved OCR accuracy
* Mobile-friendly UI
* Word problem solving with AI

---

## License

This project is for educational and research purposes.

---

## Author

Developed as an AI-powered educational tool for solving algebra problems from images.
