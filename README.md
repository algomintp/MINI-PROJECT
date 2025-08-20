📞 Phone Number Cleanup Automation (UiPath)
📌 Overview

This UiPath automation cleans up phone numbers stored in an Excel file. It removes unwanted special characters (like -, (, ), spaces), validates phone numbers to ensure they contain exactly 10 digits, and writes the cleaned list into a new sheet within the same Excel file.

⚙️ Workflow Steps

Read Input File

Use Read Range to load data from the Excel sheet containing the Phone Numbers column.

Process Each Phone Number

Apply Regex.Replace(phone, "\D", "") to strip non-digit characters.

Check if the cleaned number length equals 10 digits.

If valid, store it in a new DataTable.

Write Output

Use Write Range to write the cleaned valid numbers to a new sheet (e.g., Cleaned_Numbers) in the same Excel file.

🛠 Requirements

UiPath Studio installed

Excel Application Scope (Excel package)

Input Excel file with a column named Phone Numbers

🚀 How to Run

Open UiPath Studio.

Load the project and update the file path in Excel Application Scope.

Run the automation.

Check the new sheet (Cleaned_Numbers) for valid, cleaned phone numbers.

✅ Example

Input (Phone Numbers):

(123) 456-7890

987-654-321

111 222 3333

Output (Cleaned_Numbers):

1234567890

1112223333
