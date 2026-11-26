# 🎓 Student Grade Calculator & Management System

A beginner-friendly, menu-driven, console-based Python application that stores marks for three subjects, calculates each student's total, percentage and grade, and saves every record to a JSON file so the data is still there after you close the program.

---

## ✨ Features

- ➕ **Add** a student with a roll number, name and marks for three subjects
- 👀 **View** all records in a formatted table
- 🔍 **Search** a student by roll number and see the full record
- 🗑️ **Delete** a student record by roll number
- 🤖 **Automatic calculation** of total, percentage and grade
- 🛡️ **Input validation** for roll number, name and marks
- 💽 **Persistent storage** in `student_records.json`
- 🚨 **Error handling** for invalid input, duplicate roll numbers and corrupted data files

## 📚 Subjects

Each student is graded in three subjects:

1. Python Programming
2. Database Management
3. Discrete Mathematics

Each subject takes marks from 0 to 100, so the maximum total is 300.

## 🧮 Calculation Logic

```
Total      = Python Marks + Database Marks + Discrete Mathematics Marks
Percentage = Total / 3            (rounded to 2 decimal places)
```

The grade is based on the percentage:

| Percentage       | Grade | Remark      |
|------------------|-------|-------------|
| 90 and above     | A+ 🏆 | Outstanding |
| 80 to below 90   | A 🌟  | Excellent   |
| 70 to below 80   | B 👍  | Good        |
| 60 to below 70   | C 🙂  | Average     |
| 40 to below 60   | D ✔️  | Pass        |
| Below 40         | F ❌  | Fail        |

### 🧾 Example Calculation

Suppose a student gets:

- Python: 85
- DBMS: 78
- Maths: 92

Then:

- **Total Marks:** 85 + 78 + 92 = 255 out of 300
- **Percentage:** 255 ÷ 3 = 85%
- **Grade:** A 🌟

## 📁 Project Structure

```
Python-Major-Project-main/
└── Student Grade Calculator Using Python/
    └── Student_Grade_Calculator.ipynb    # Main program (Jupyter Notebook)
```

The notebook is organised into sections: imports and configuration, data loading and saving, grade calculation, add, view, search and delete operations, the main menu loop, and the run cell.

## 🛠️ Requirements

- 🐍 Python 3.x
- 📓 Jupyter Notebook or JupyterLab, or any editor that can run Python

No third-party libraries are needed. The program uses only the standard library modules `json` and `os`.

**Technologies used:** Python 3, Jupyter Notebook, JSON file storage

## 🚀 How to Run

### 📓 Option 1: Jupyter Notebook

1. Open the folder `Student Grade Calculator Using Python/`.
2. Start Jupyter:
   ```bash
   jupyter notebook
   ```
3. Open `Student_Grade_Calculator.ipynb` and choose **Cell → Run All**.
4. The menu appears in the last cell. Type a choice and press Enter.

#### 📦 Installing Jupyter (if needed)

If Jupyter Notebook is not installed, run this in your terminal:

```bash
pip install notebook
```

Then start it with `jupyter notebook`, as shown above.

### 🐍 Option 2: Run as a Python script

Copy the code from the notebook cells into one file, for example `student_grade.py`, and run:

```bash
python student_grade.py
```

The program creates `student_records.json` in the current folder when the first record is saved.

## 🖥️ Usage

When the program starts, this menu is shown:

```
=============================================
     MCA 1ST SEM: STUDENT GRADE SYSTEM
=============================================
 1. Add New Student Record
 2. View All Student Records
 3. Search Student by Roll Number
 4. Delete Student Record
 5. Exit Program
=============================================
```

### ✅ Input Validation Rules

- The roll number cannot be empty and must not already exist (for example, `MCA202601`).
- The name cannot be empty and may contain only letters and spaces.
- Each mark must be a number from 0 to 100.
- Any menu choice other than 1 to 5 shows an error and the menu appears again.

If a check fails, an error message is printed and no record is changed.

### 📋 Example Output

Viewing records prints a table like this (sample data):

```
———————————————————————————————————————————————————————————————————————————
Roll No      | Student Name         | Total    | Percentage | Grade
———————————————————————————————————————————————————————————————————————————
MCA202601    | Aarav Sharma         | 275.0    | 91.67     % | A+ (Outstanding)
MCA202602    | Riya Verma           | 210.0    | 70.0      % | B (Good)
———————————————————————————————————————————————————————————————————————————
```

## 💾 Data Storage

Records are saved in `student_records.json`. The roll number is the key, and the value holds the student's details:

```json
{
    "MCA202601": {
        "name": "Aarav Sharma",
        "marks": {
            "Python Programming": 92.0,
            "Database Management": 88.0,
            "Discrete Mathematics": 95.0
        },
        "total": 275.0,
        "percentage": 91.67,
        "grade": "A+ (Outstanding)"
    }
}
```

If the file does not exist, the program starts with no records. If the file is corrupted, a warning is shown and the program starts with no records.

## 🧠 Concepts Demonstrated

- 🔤 Variables and constants
- 🧩 Functions
- 🗂️ Nested dictionaries
- 🔀 Conditional statements (`if` / `elif` / `else`)
- 🔁 Loops (`while True` menu loop and `for` loop for the table)
- 🧯 Exception handling (`ValueError`, `JSONDecodeError`, `IOError`)
- 📂 File handling with `open()` and `with`
- ✂️ String methods and f-string formatting

## 📝 Important Notes

- Run the notebook cells in order, from top to bottom.
- The menu uses `input()`, so run the notebook in an environment that supports interactive input, such as Jupyter Notebook or JupyterLab.
- Each student must have a unique roll number.
- Marks must be numeric values between **0 and 100**.
- Records are saved to `student_records.json`, so they remain after the program ends.

## ⚠️ Limitations

- 🖥️ Console interface only, with no graphical interface
- ✏️ Existing records cannot be edited; a record must be deleted and added again
- 📌 Only three fixed subjects are supported
- ⚖️ The grade depends only on the overall percentage, so a student can pass with very low marks in one subject
- ⚠️ Records are deleted immediately, with no confirmation prompt
- 🔒 Single-user, with no login or password
- ❗ If one mark is invalid, the whole entry must be typed again

## 🔮 Future Scope

- ✏️ Edit an existing record
- 📝 Pass marks and a pass/fail result for each subject
- 🔢 Support a variable number of subjects
- 🏅 Rank lists and class averages
- 📤 Export results to CSV or Excel
- 🗄️ Replace the JSON file with SQLite or another database
- 🎨 Graphical interface using Tkinter, or a web interface
- 🔐 Login system and a confirmation step before deleting

## 🎯 Learning Outcomes

By working through this project, you can practise:

- Python functions and return values
- `if`, `elif`, and `else` conditional statements
- `while` and `for` loops
- Dictionaries and nested dictionaries
- User input and type conversion
- Exception handling with `try` and `except`
- File handling with JSON
- Input validation and menu-driven programming

## 👤 Author

**Mohammad Azeem**

🔗 [GitHub: Azeem-004](https://github.com/Azeem-004)


