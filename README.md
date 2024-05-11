# Password Manager

## Overview
The Password Manager is a command-line based application developed in Python. It generates passwords of user-defined length and provides an option to save them in a designated folder. The application utilizes the `random` and `string` libraries for password generation and relies on `openpyxl` and `xlsxwriter` for reading from and writing to Excel files.

## Features
- **Password Generation:** Users can specify the desired length for the password. The application generates a random password using a combination of digits, uppercase and lowercase letters.
  
- **Password Saving:** Users have the option to save the generated password along with a name and timestamp. The saved passwords are stored in an Excel file within a designated folder.

## Code Structure

### Modules Used
- `time`: For timestamp generation.
- `random` and `string`: For password generation.
- `os`: For handling file paths.
- `openpyxl`: For reading Excel files.
- `xlsxwriter`: For writing to Excel files.

### Functions
- `reader()`: Reads data from the Excel file where passwords are saved.
- `writters(data)`: Writes data to the Excel file, including the newly generated password if the user chooses to save it.
  
### Main Execution
- The program begins by prompting the user to enter the desired length of the password.
- If the entered length is less than 8, the program requests the user to enter a longer length.
- Once a valid length is entered, a random password is generated.
- The user is then asked if they want to save the password.
- If the user chooses to save, they are prompted to enter a name for the password entry.
- The current timestamp is automatically recorded.
- The password, along with its associated name and timestamp, is saved to the Excel file.

## File Structure
- The Excel file (`save_folder.xlsx`) is stored in the same directory as the Python script.
- The Excel file contains four columns: Serial Number, Date, Name, and Password.
- Password entries are appended to the existing data in the Excel file.

## Usage
1. Execute the Python script.
2. Follow the prompts to generate and optionally save passwords.

## Potential Improvements
- Implement encryption for saved passwords to enhance security.
- Add functionality to retrieve passwords based on name or date.
- Create a graphical user interface (GUI) for improved user experience.

## Conclusion
The Password Manager provides a simple yet effective solution for generating and managing passwords via the command line. It offers flexibility in password length and provides the convenience of saving passwords for future reference. With further enhancements, it can become a robust tool for personal and professional use.
