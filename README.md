# 🎓 Student Management System (C++ Case Study)

An Object-Oriented Programming (OOP) console-based application designed to manage, process, and persist student academic records without requiring an external database management system[cite: 8, 9].

---

## 📌 Project Overview

| Attribute | Details |
| :--- | :--- |
| **🏫 Institution** | Chandigarh University — University Institute of Computing[cite: 8] |
| **📚 Course Code & Name** | 25CAH-201: Object Oriented Programming[cite: 8] |
| **👤 Author** | RAKSHAK (UID: 25BCD10102)[cite: 8] |
| **🎓 Program & Section** | BCA (Data Science), Semester 3, Section 25BCD2(A)[cite: 8] |
| **👨‍🏫 Submitted To** | Mr. Jitendra Kumar (Professor)[cite: 8] |
| **💻 Language & Standard** | C++ (C++17 standard)[cite: 10, 11] |
| **💾 Storage Engine** | Delimited plain text file (`students.txt`)[cite: 9, 10] |

---

## 🚀 Key Features

* ➕ **Add Student:** Captures student ID, name, age, course, and marks while verifying input and rejecting duplicate IDs[cite: 10, 11].
* 📋 **Display All Records:** Outputs stored records into an aligned console table along with calculated grades[cite: 10, 11].
* 🔍 **Search by ID:** Finds and displays individual student records matching a query ID[cite: 10, 11].
* ✏️ **Update Student:** Edits details of existing entries with validation checks[cite: 10, 11].
* ❌ **Delete Student:** Removes selected records from memory and updates the storage file[cite: 10, 11].
* 📊 **Automated Grading:** Assigns letter grades ($A+$, $A$, $B$, $C$, $D$, $F$) according to entered marks[cite: 11, 12].
* 🛡️ **Defensive Input Handling:** Validates numeric ranges and input buffers to prevent parsing failures and infinite loops[cite: 10, 13].

---

## 🛠️ Tools & Technologies

* **Programming Language:** C++17[cite: 10, 11]
* **Compiler:** MSYS2 $g++$[cite: 10, 11]
* **Editor:** Visual Studio Code[cite: 10]
* **Standard Library Utilities:**
  * `<vector>` — Dynamic collection storing `Student` objects during runtime[cite: 10, 12].
  * `<fstream>` & `<sstream>` — Stream handling for reading from and writing to persistent storage[cite: 10, 11, 13].
  * `<iomanip>` — Output alignment and table formatting[cite: 12, 13].

---

## 🏛️ System Design & Class Architecture

* **`Student` Class:** Encapsulates private data members (`id`, `name`, `age`, `course`, and `marks`) and exposes public methods to fetch the identifier, compute letter grades, display aligned records, and serialize data for file saving[cite: 10, 12].
* **`StudentManager` Class:** Controls runtime workflows, coordinates the `std::vector<Student>` collection, loads records upon initialization, saves data after modifications, and executes input validation[cite: 10, 12, 13, 14].

---

## 🗄️ File Storage Format

Records are saved line by line inside `students.txt` using the vertical bar delimiter (`|`)[cite: 10]:

```text
101|Aman Sharma|19|BCA|85
102|Priya Singh|20|BCA Data Science|92
```

> ⚠️ **Note:** Name and course fields cannot contain the `|` character to avoid field parsing corruption[cite: 10, 13].

---

## 📋 Grade Mapping Scale

| Marks Range | Assigned Grade |
| :---: | :---: |
| $\text{Marks} \ge 90$ | **A+**[cite: 12] |
| $80 \le \text{Marks} < 90$ | **A**[cite: 12] |
| $70 \le \text{Marks} < 80$ | **B**[cite: 12] |
| $60 \le \text{Marks} < 70$ | **C**[cite: 12] |
| $50 \le \text{Marks} < 60$ | **D**[cite: 12] |
| $\text{Marks} < 50$ | **F**[cite: 12] |

---

## 🧪 Validation & Constraints

* **Student ID:** Must be a positive integer ($> 0$) and strictly unique[cite: 11, 14].
* **Age:** Must be between $1$ and $120$[cite: 11, 14].
* **Marks:** Must be a numeric value between $0.00$ and $100.00$[cite: 11, 13].
* **Text Strings:** Must not be empty and must not contain the `|` delimiter[cite: 11, 13].

---

## 💻 Compilation & Execution

### 1️⃣ Compile
Ensure an environment with a C++17 compiler (such as GCC/MSYS2) is installed[cite: 10, 11]. Compile `main.cpp` using:

```bash
g++ -std=c++17 main.cpp -o student_management
```

### 2️⃣ Run
Execute the binary in the directory containing or intended to hold `students.txt`[cite: 11]:

```bash
# Windows
student_management.exe

# Linux / macOS
./student_management
```

---

## 🖥️ Sample Console Output

```text
====================================
     STUDENT MANAGEMENT SYSTEM      
====================================
1. Add Student
2. Display All Students
3. Search Student
4. Update Student
5. Delete Student
0. Exit
====================================
Enter your choice: 2

--- All Students ---
ID      Name                  Age     Course            Marks     Grade
----------------------------------------------------------------------------
101     Arun Sharma           20      Computer Science  85.50     A
102     Jane Smith            21      Mathematics       92.00     A+
103     Michael Chang         19      Physics           74.00     B
104     Priya Patel           22      Chemistry         68.50     C
```
*(Reference: System run output[cite: 16])*

---

## 🔮 Limitations & Future Improvements

* 🗃️ **Database Engine:** Replace flat-text persistence with an embedded database like SQLite for ACID compliance and safer updates[cite: 16].
* 📊 **Reporting & Analytics:** Add functionalities for class mark averages, sorting (by name or grade), and top-performer filters[cite: 16].
* 🔐 **Authentication & Access Control:** Introduce role-based login to protect sensitive academic records[cite: 9, 16].
* 🧩 **Modular Architecture:** Refactor code into distinct `.h` header and `.cpp` implementation files[cite: 16].
