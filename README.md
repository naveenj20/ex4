## NAME: NAVEEN JAISANKER
## REG. NO.:212224110039

EXERCISE-4

# AIM:

To develop a UiPath workflow that reads data from an Excel file and writes it into another Excel file using modern Excel activities.

# PROCEDURE:

Step 1: Create Project

Open UiPath Studio → Create a new Process (Sequence/Flowchart based).

Name it ReadWriteExcel.

Step 2: Read Data from Excel

Drag an Excel Process Scope.

Inside it, add a Use Excel File activity → point to input.xlsx.

Inside Use Excel File:

Insert a Read Range activity.

Set Sheet Name = "Sheet1".

Leave Range blank to read all rows.

Store the output in a variable dataTable (type System.Data.DataTable).

Step 3: Write Data to Excel

Add another Use Excel File activity → point to output.xlsx.

Inside it, insert Write DataTable to Excel activity.

What to write = dataTable.

Destination = ExcelFile.Sheet("Sheet1") (use the resource name created by UiPath).

Tick Include Headers to copy column names.

# WORKFLOW:

Your workflow consists of:

Excel Process Scope

Use Excel File (input.xlsx)

Read Range → dataTable

Use Excel File (output.xlsx)

Write DataTable to Excel → writes dataTable to "Sheet1"

# OUTPUT:

Input Excel Sheet:
<img width="1919" height="581" alt="Screenshot 2025-09-05 185833" src="https://github.com/user-attachments/assets/44b83768-d6fe-4a69-a4d2-ba92d77d353c" />

Output Excel Sheet (before execution):
<img width="1909" height="602" alt="Screenshot 2025-09-05 185843" src="https://github.com/user-attachments/assets/0fbf9199-d5ba-42bd-9d06-fb178db68717" />

Output Excel Sheet (after execution):
<img width="1919" height="573" alt="Screenshot 2025-09-05 185903" src="https://github.com/user-attachments/assets/316805fb-2fa1-4e04-96f7-50821acda295" />

The contents of input.xlsx are successfully copied into output.xlsx.


# RESULT:

Thus, the UiPath workflow for reading data from one Excel file and writing it to another Excel file was executed successfully.
