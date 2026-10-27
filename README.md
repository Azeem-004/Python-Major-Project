# 🎓 Student Grade Calculator

A beginner-friendly Python project that helps manage student records and calculate grades based on marks in three subjects: **Python, DBMS, and Maths**. This project uses core Python concepts such as functions, dictionaries, loops, conditional statements, and input validation.

## ✨ Features

- **Add Student Record** — enter a student's roll number, name, and marks.
- **Calculate Total Marks** — adds marks from Python, DBMS, and Maths.
- **Calculate Percentage** — calculates the average percentage across the three subjects.
- **Assign Grade Automatically** — determines the grade from the percentage.
- **View All Students** — displays all student records entered during the current session.
- **Search Student** — find a student using their roll number.
- **Input Validation** — checks for duplicate roll numbers, non-numeric marks, and marks outside the 0–100 range.

## 📊 Grading Criteria

| Percentage | Grade |
|---|---|
| 90% and above | A+ |
| 80% to below 90% | A |
| 70% to below 80% | B |
| 60% to below 70% | C |
| 40% to below 60% | D |
| Below 40% | Fail |

## 🛠️ Technologies Used

- **Language:** Python 3
- **Environment:** Jupyter Notebook
- **Libraries:** No external libraries required

## 📁 Project Structure

```text
Student-Grade-Calculator/
├── Student_Grade_Calculator.ipynb
└── README.md
```

## 🚀 Getting Started

### Option 1: Run in Jupyter Notebook

1. Download or clone this project.
2. Open Jupyter Notebook or JupyterLab.
3. Upload and open `Student_Grade_Calculator.ipynb`.
4. Run the notebook cells in order.
5. Follow the on-screen menu to add, view, or search student records.

### Option 2: Install Jupyter (if needed)

If Jupyter Notebook is not installed, run this command in your terminal:

```bash
pip install notebook
```

Then start Jupyter Notebook:

```bash
jupyter notebook
```

## 🧭 How to Use

When the program runs, it displays a menu:

1. **Add Student Record** — enter a unique roll number, student's name, and marks for Python, DBMS, and Maths.
2. **View All Students** — see all records entered in the current run.
3. **Search Student by Roll No** — enter a roll number to find a specific record.
4. **Exit** — close the program.

### Example Calculation

Suppose a student gets:

- Python: 85
- DBMS: 78
- Maths: 92

Then:

- **Total Marks:** 85 + 78 + 92 = 255 out of 300
- **Percentage:** 255 ÷ 3 = 85%
- **Grade:** A

## ⚠️ Important Notes

- Marks must be numeric values between **0 and 100**.
- Each student must have a unique roll number.
- Records are stored in memory only. They are **not saved to a file or database**, so they are lost when the program ends.
- The notebook uses an interactive menu with `input()`. Run it in a Jupyter environment that supports interactive input.

## 🎯 Learning Outcomes

By completing this project, you can practise:

- Python functions and return values
- `if`, `elif`, and `else` conditional statements
- `while` and `for` loops
- Dictionaries and nested dictionaries
- User input and type conversion
- Exception handling with `try` and `except`
- Basic validation and menu-driven programming

## 👨‍💻 Author

**Mohammad Azeem**

---

⭐ If you find this project useful for learning Python fundamentals, feel free to use it as a practice project.
