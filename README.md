#Brute Force PDF Password Cracker
Description: This Python script is a brute force password cracker specifically designed to crack numeric passwords protecting PDF files. It uses the PyPDF2 library to interact with the PDF file and the itertools library to generate all possible combinations of numeric characters.

Usage:

Install Required Libraries: Run pip install PyPDF2 to install the required library.
Modify the Script: Update the file_path variable with the path to the protected PDF file and the max_length variable with the maximum length of the password you want to try.
Run the Script: Execute the script using Python (e.g., python brute_force_pdf_password.py).
Script Explanation:

The script uses a brute force approach to try all possible combinations of numeric characters up to the specified max_length. It iterates through each length from 1 to max_length and generates all possible combinations of numeric characters using the itertools.product function.

For each generated password, the script attempts to decrypt the PDF file using the PyPDF2.PdfReader.decrypt method. If the decryption is successful, the script prints the password and returns it. If an error occurs during the decryption process, the script catches the exception and continues to the next password attempt.

Example Usage:

The script includes an example usage section at the end, which demonstrates how to use the script to crack a protected PDF file. Simply update the file_path variable with the path to your protected PDF file and adjust the max_length variable as needed.

Limitations:

Numeric Characters Only: This script is designed to crack passwords composed of numeric characters only. If the password contains letters or special characters, this script will not be effective.
Performance: The script's performance decreases as the max_length increases. Be prepared for longer execution times for longer passwords.
PDF File Size: The script's performance may also be affected by the size of the PDF file. Larger files may take longer to decrypt.
