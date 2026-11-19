
# 🔐 WEEK 3 – PASSWORD CRACKING PRACTICAL
### Cybersecurity & Ethical Hacking | Password Security and Hash Analysis

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-blue?style=for-the-badge)
![Week](https://img.shields.io/badge/Week-03-purple?style=for-the-badge)
![Practical](https://img.shields.io/badge/Practical-Completed-success?style=for-the-badge)
![Tools](https://img.shields.io/badge/Tools-JTR%20%7C%20Networkwalks-orange?style=for-the-badge)

---

# 📌 PROJECT OVERVIEW

This repository contains the documentation for the Week 3 Cybersecurity and Ethical Hacking practical exercises.

The exercises focused on password cracking, password hash extraction, and password recovery from encrypted PDF documents.

Two practical modules were completed using different password-cracking approaches:

- **Project Module 1:** Password Cracking with John the Ripper (JTR) and Johnny GUI.
- **Project Module 2:** Password Cracking with Networkwalks Tools.

For Module 1, three separate password-protected PDF documents were processed using John the Ripper. Each document produced an individual password-cracking result.

Module 2 introduced the use of Networkwalks online tools to extract PDF password hashes and attempt password recovery.

The practical exercises provided hands-on experience with password security, hash extraction, and the importance of strong password protection.

---

# 🎯 PROJECT OBJECTIVES

The objectives of these practical exercises were to:

- Understand password cracking and password hashing.
- Identify how password-protected PDF documents are secured.
- Extract password hashes from encrypted PDF files.
- Install and configure John the Ripper and Johnny GUI.
- Use John the Ripper to perform password-cracking attacks.
- Use Networkwalks tools to extract and crack PDF hashes.
- Verify recovered passwords by opening protected PDF documents.
- Understand the importance of strong and unique passwords.

---

# 🛠️ TOOLS AND TECHNOLOGIES

| Tool | Purpose |
|---|---|
| John the Ripper | Password-cracking software |
| Johnny GUI | Graphical interface for John the Ripper |
| PDF Hash Extractor | Extracts hashes from protected PDF documents |
| Notepad | Saves extracted hash values |
| Networkwalks Hash Calculator | Generates PDF password hashes |
| Networkwalks Password Cracker | Attempts password recovery |
| Windows PC | Operating environment |
| Web Browser | Accesses online tools |

## 🔗 TOOL REFERENCES

- [John the Ripper Official Website](https://www.openwall.com/john/)
- [Johnny GUI](https://openwall.info/wiki/john/johnny)
- [Online PDF Hash Extractor](https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php)
- [Networkwalks Practical Lab](https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/)
- [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)
- [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)

---

# 🔵 PROJECT MODULE 1: PASSWORD CRACKING WITH JOHN THE RIPPER

## 1.1 Background

John the Ripper (JTR) is a password-cracking tool commonly used by cybersecurity professionals to evaluate password strength.

It supports different password hash formats and can be used to test the security of password-protected files, including PDF documents.

Johnny is the graphical user interface for John the Ripper. It provides a more accessible way to interact with JTR without relying entirely on command-line instructions.

This practical involved using both John the Ripper and Johnny GUI to recover passwords from three separate protected PDF documents.

## 1.2 Task

Use John the Ripper and Johnny GUI on a Windows PC to crack the passwords of three protected PDF documents:

1. lockedpdf1
2. lockedpdf2
3. lockedpdf3

Each document was processed separately, and the results were documented individually.

---

## 1.3 PROCEDURE AND IMPLEMENTATION

### STEP 1 – Download John the Ripper

John the Ripper was downloaded from the official Openwall website.

The downloaded files were extracted to the computer in preparation for installation and configuration.

**Screenshot 1 – John the Ripper Download**

![JTR Download](screenshots/JTR/01-jtr-download.png)

**Screenshot 2 – Extracted John the Ripper Files**

![JTR Extracted Files](screenshots/JTR/02-jtr-extracted-files.png)

---

### STEP 2 – Download and Install Johnny GUI

Johnny GUI was downloaded from the official website.

The installation file was opened, and the setup instructions were followed to complete the installation.

**Screenshot 3 – Johnny GUI Download**

![Johnny Download](screenshots/JTR/03-johnny-download.png)

**Screenshot 4 – Johnny Installation**

![Johnny Installation](screenshots/JTR/04-johnny-installation.png)

**Screenshot 5 – Johnny GUI Opened**

![Johnny Interface](screenshots/JTR/05-johnny-interface.png)

---

### STEP 3 – Configure Johnny GUI

After installation, Johnny was opened.

The settings option was selected to configure the application and locate the John the Ripper executable.

The `john.exe` file was located inside the `run` folder within the extracted John the Ripper directory.

The executable was selected to allow Johnny to communicate with John the Ripper.

**Screenshot 6 – Johnny Settings**

![Johnny Settings](screenshots/JTR/06-johnny-settings.png)

**Screenshot 7 – Locating john.exe**

![Locate John Executable](screenshots/JTR/07-locate-john-exe.png)

**Screenshot 8 – John Executable Selected**

![John Executable Selected](screenshots/JTR/08-john-exe-selected.png)

---

### STEP 4 – Download the Protected PDF Documents

Three password-protected PDF documents were selected for the exercise.

The documents were saved locally before beginning the hash extraction process.

**Screenshot 9 – First Protected PDF**

![Locked PDF 1](screenshots/JTR/09-lockedpdf1.png)

**Screenshot 10 – Second Protected PDF**

![Locked PDF 2](screenshots/JTR/10-lockedpdf2.png)

**Screenshot 11 – Third Protected PDF**

![Locked PDF 3](screenshots/JTR/11-lockedpdf3.png)

---

### STEP 5 – Extract the PDF Password Hashes

The Online PDF Hash Extractor was accessed through a web browser.

Each protected PDF document was uploaded individually to extract its corresponding password hash.

The extracted hash values were copied for use in John the Ripper.

The hash values were expected to begin with `$pdf$`.

**Screenshot 12 – PDF Hash Extractor Website**

![PDF Hash Extractor](screenshots/JTR/12-pdf-hash-extractor.png)

**Screenshot 13 – Uploading lockedpdf1**

![Upload PDF 1](screenshots/JTR/13-upload-lockedpdf1.png)

**Screenshot 14 – Hash Extracted for lockedpdf1**

![Hash PDF 1](screenshots/JTR/14-hash-lockedpdf1.png)

**Screenshot 15 – Hash Extracted for lockedpdf2**

![Hash PDF 2](screenshots/JTR/15-hash-lockedpdf2.png)

**Screenshot 16 – Hash Extracted for lockedpdf3**

![Hash PDF 3](screenshots/JTR/16-hash-lockedpdf3.png)

**Note:** If the extracted hash contains additional characters such as `b'` at the beginning, these should be removed before saving the hash file. The hash should retain the correct `$pdf$` format.

---

### STEP 6 – Save the Extracted Hash Values

Notepad was opened to store the extracted hash values.

Each hash was saved in a text file for use in the cracking process.

The first hash file was saved as `hash1.txt`. Separate files were prepared for the other PDF documents to keep the results organized.

**Screenshot 17 – Hash Pasted into Notepad**

![Hash in Notepad](screenshots/JTR/17-hash-notepad.png)

**Screenshot 18 – Saving Hash1.txt**

![Save Hash 1](screenshots/JTR/18-save-hash1.png)

**Screenshot 19 – Saving Hash2.txt**

![Save Hash 2](screenshots/JTR/19-save-hash2.png)

**Screenshot 20 – Saving Hash3.txt**

![Save Hash 3](screenshots/JTR/20-save-hash3.png)

---

### STEP 7 – Import Hash Files into Johnny

Johnny was reopened.

The Open Password File option was selected, and the saved hash text file was imported.

This process was repeated for each of the three PDF documents.

**Screenshot 21 – Open Password File**

![Open Password File](screenshots/JTR/21-open-password-file.png)

**Screenshot 22 – Importing lockedpdf1 Hash**

![Import Hash 1](screenshots/JTR/22-import-hash1.png)

**Screenshot 23 – Importing lockedpdf2 Hash**

![Import Hash 2](screenshots/JTR/23-import-hash2.png)

**Screenshot 24 – Importing lockedpdf3 Hash**

![Import Hash 3](screenshots/JTR/24-import-hash3.png)

---

### STEP 8 – Start the Password-Cracking Attack

After importing each hash file, the Start New Attack option was selected.

John the Ripper began processing the hash and attempting to recover the corresponding password.

The process was performed separately for each PDF document.

The time required depended on the computer's processing speed and the complexity of the password.

**Screenshot 25 – Starting Attack on lockedpdf1**

![Start Attack 1](screenshots/JTR/25-start-attack1.png)

**Screenshot 26 – Starting Attack on lockedpdf2**

![Start Attack 2](screenshots/JTR/26-start-attack2.png)

**Screenshot 27 – Starting Attack on lockedpdf3**

![Start Attack 3](screenshots/JTR/27-start-attack3.png)

---

## 1.4 RESULTS AND SCREENSHOTS

The three protected PDF documents were processed individually using John the Ripper.

Each document produced a different password-cracking result.

The screenshots below provide placeholders for the individual results obtained during the practical.

### RESULT 1 – lockedpdf1

**Description:** Password-cracking result for the first protected PDF document.

**Screenshot:**

![lockedpdf1 Cracking Result](screenshots/JTR/28-lockedpdf1-result.png)

**PDF Verification:**

![lockedpdf1 Opened](screenshots/JTR/29-lockedpdf1-verified.png)

---

### RESULT 2 – lockedpdf2

**Description:** Password-cracking result for the second protected PDF document.

**Screenshot:**

![lockedpdf2 Cracking Result](screenshots/JTR/30-lockedpdf2-result.png)

**PDF Verification:**

![lockedpdf2 Opened](screenshots/JTR/31-lockedpdf2-verified.png)

---

### RESULT 3 – lockedpdf3

**Description:** Password-cracking result for the third protected PDF document.

**Screenshot:**

![lockedpdf3 Cracking Result](screenshots/JTR/32-lockedpdf3-result.png)

**PDF Verification:**

![lockedpdf3 Opened](screenshots/JTR/33-lockedpdf3-verified.png)

---

## 1.5 MODULE 1 SUMMARY

The first module provided practical experience using John the Ripper and Johnny GUI to recover passwords from encrypted PDF documents.

Three separate PDF files were processed, with individual hash extraction, import, cracking, and result verification.

The exercise demonstrated how password hashes can be extracted and used in password-cracking tools to evaluate the strength of document passwords.

---

# 🟣 PROJECT MODULE 2: PASSWORD CRACKING WITH NETWORKWALKS TOOLS

## 2.1 Background

The second practical exercise focused on using Networkwalks online tools to extract and crack passwords from protected PDF documents.

The exercise involved two main tools:

- Networkwalks Hash Calculator
- Networkwalks Password Cracker

Unlike the first module, which required installing software, these tools were accessed directly through a web browser.

The Hash Calculator was used to generate the PDF password hash, while the Password Cracker attempted to recover the original password from that hash.

## 2.2 Task

Use the Networkwalks Hash Calculator and Password Cracker tools on a Windows laptop to recover the password of the provided protected PDF document.

---

## 2.3 PROCEDURE AND IMPLEMENTATION

### STEP 1 – Download the Encrypted PDF

The Networkwalks practical lab webpage was accessed.

The protected PDF document, identified in the lab instructions as `My Locked PDF1.pdf`, was downloaded to the computer.

**Screenshot 1 – Networkwalks Lab Page**

![Networkwalks Lab](screenshots/Networkwalks/01-networkwalks-lab.png)

**Screenshot 2 – Downloaded Protected PDF**

![Downloaded PDF](screenshots/Networkwalks/02-downloaded-pdf.png)

---

### STEP 2 – Open the Networkwalks Hash Calculator

The Networkwalks Hash Calculator was opened using the web browser.

The tool was prepared to receive the protected PDF document.

**Screenshot 3 – Hash Calculator Website**

![Hash Calculator](screenshots/Networkwalks/03-hash-calculator.png)

---

### STEP 3 – Upload the Protected PDF

The protected PDF document was uploaded to the Hash Calculator.

The tool processed the file and generated its corresponding PDF password hash.

**Screenshot 4 – Selecting the PDF File**

![Select PDF](screenshots/Networkwalks/04-select-pdf.png)

**Screenshot 5 – PDF Uploaded**

![PDF Uploaded](screenshots/Networkwalks/05-pdf-uploaded.png)

---

### STEP 4 – Copy the Extracted Hash

After the file was processed, the generated hash was displayed.

The complete hash value was copied for use in the Password Cracker.

The hash began with `$pdf$`.

**Screenshot 6 – Generated PDF Hash**

![Generated Hash](screenshots/Networkwalks/06-generated-hash.png)

**Screenshot 7 – Copying the Complete Hash**

![Copy Hash](screenshots/Networkwalks/07-copy-hash.png)

---

### STEP 5 – Open the Networkwalks Password Cracker

The Networkwalks Password Cracker was accessed through the web browser.

The tool was prepared to receive the extracted hash value.

**Screenshot 8 – Password Cracker Website**

![Password Cracker](screenshots/Networkwalks/08-password-cracker.png)

---

### STEP 6 – Submit the Hash and Start the Attack

The copied PDF hash was pasted into the Password Cracker.

The Start Attack option was selected to begin the password-recovery process.

The tool attempted different password combinations until a match was found or the attempt concluded.

**Screenshot 9 – Hash Entered into Password Cracker**

![Hash Entered](screenshots/Networkwalks/09-hash-entered.png)

**Screenshot 10 – Password-Cracking Process Started**

![Attack Started](screenshots/Networkwalks/10-attack-started.png)

---

### STEP 7 – Review the Cracking Result

The Password Cracker was allowed to complete its process.

The result displayed by the tool was reviewed.

The time taken depended on the complexity of the password.

**Screenshot 11 – Password-Cracking Result**

![Cracking Result](screenshots/Networkwalks/11-cracking-result.png)

---

### STEP 8 – Verify the Recovered Password

The protected PDF document was opened.

The recovered password was entered to confirm that the document could be accessed successfully.

**Screenshot 12 – Entering the Recovered Password**

![Enter Password](screenshots/Networkwalks/12-enter-password.png)

**Screenshot 13 – Successfully Opened PDF**

![PDF Opened](screenshots/Networkwalks/13-pdf-opened.png)

---

## 2.4 MODULE 2 SUMMARY

The second module demonstrated how Networkwalks online tools can be used to extract PDF password hashes and attempt password recovery.

The Hash Calculator generated the hash, which was then submitted to the Password Cracker.

The recovered password was tested against the protected PDF document to verify the result.

This exercise provided additional insight into password cracking using browser-based cybersecurity tools.

---

# 📚 KEY LEARNINGS

The Week 3 practical exercises provided hands-on experience in password security and password-cracking techniques.

The main lessons learned include:

### 1. Password Hashing
Developed an understanding of how passwords are represented through cryptographic hashes.

### 2. Hash Extraction
Learned how to extract password hashes from encrypted PDF documents using online tools.

### 3. John the Ripper
Gained practical experience installing, configuring, and using John the Ripper with Johnny GUI.

### 4. Password Cracking
Learned how password-cracking tools process hashes and attempt to identify the original password.

### 5. Networkwalks Tools
Gained experience using online tools to calculate PDF hashes and attempt password recovery.

### 6. Password Verification
Understood the importance of testing recovered passwords against the original protected documents.

### 7. Password Security
Recognized the importance of strong, unique, and complex passwords in protecting sensitive information.

---

# 🔒 SECURITY RECOMMENDATIONS

Based on the exercises completed, the following security practices are recommended:

- Use long and complex passwords.
- Avoid common words and predictable password combinations.
- Use unique passwords for different accounts and documents.
- Consider using a reputable password manager.
- Protect sensitive documents with strong encryption.
- Avoid sharing passwords and password hashes with unauthorized individuals.
- Use multi-factor authentication where available.
- Regularly review password security practices.

---

# 📝 CONCLUSION

The Week 3 practical exercises provided valuable hands-on experience in password cracking, hash extraction, and password security.

The first module focused on using John the Ripper and Johnny GUI to process three separate password-protected PDF documents. Each document was handled individually, producing three different password-cracking results.

The second module introduced Networkwalks online tools, demonstrating how PDF password hashes can be extracted and submitted for password recovery.

Overall, the exercises strengthened my understanding of password protection, hash analysis, and the methods used by cybersecurity professionals to evaluate password security.

The practical activities also highlighted the importance of creating strong passwords to reduce the risk of unauthorized access.

---

# 📂 REPOSITORY STRUCTURE

The following folder structure can be used to organize the documentation and practical screenshots.

```text
Week-3-Password-Cracking/
│
├── README.md
│
├── screenshots/
│   │
│   ├── JTR/
│   │   ├── 01-jtr-download.png
│   │   ├── 02-jtr-extracted-files.png
│   │   ├── 03-johnny-download.png
│   │   ├── 04-johnny-installation.png
│   │   ├── 05-johnny-interface.png
│   │   ├── 06-johnny-settings.png
│   │   ├── 07-locate-john-exe.png
│   │   ├── 08-john-exe-selected.png
│   │   ├── 09-lockedpdf1.png
│   │   ├── 10-lockedpdf2.png
│   │   ├── 11-lockedpdf3.png
│   │   ├── 12-pdf-hash-extractor.png
│   │   ├── 13-upload-lockedpdf1.png
│   │   ├── 14-hash-lockedpdf1.png
│   │   ├── 15-hash-lockedpdf2.png
│   │   ├── 16-hash-lockedpdf3.png
│   │   ├── 17-hash-notepad.png
│   │   ├── 18-save-hash1.png
│   │   ├── 19-save-hash2.png
│   │   ├── 20-save-hash3.png
│   │   ├── 21-open-password-file.png
│   │   ├── 22-import-hash1.png
│   │   ├── 23-import-hash2.png
│   │   ├── 24-import-hash3.png
│   │   ├── 25-start-attack1.png
│   │   ├── 26-start-attack2.png
│   │   ├── 27-start-attack3.png
│   │   ├── 28-lockedpdf1-result.png
│   │   ├── 29-lockedpdf1-verified.png
│   │   ├── 30-lockedpdf2-result.png
│   │   ├── 31-lockedpdf2-verified.png
│   │   ├── 32-lockedpdf3-result.png
│   │   └── 33-lockedpdf3-verified.png
│   │
│   └── Networkwalks/
│       ├── 01-networkwalks-lab.png
│       ├── 02-downloaded-pdf.png
│       ├── 03-hash-calculator.png
│       ├── 04-select-pdf.png
│       ├── 05-pdf-uploaded.png
│       ├── 06-generated-hash.png
│       ├── 07-copy-hash.png
│       ├── 08-password-cracker.png
│       ├── 09-hash-entered.png
│       ├── 10-attack-started.png
│       ├── 11-cracking-result.png
│       ├── 12-enter-password.png
│       └── 13-pdf-opened.png
│
└── documents/
    └── Practical-Reference-Materials/
```

---

# ⚠️ DISCLAIMER

These practical exercises were conducted for educational purposes as part of cybersecurity and ethical hacking training.

Password-cracking tools should only be used on files, systems, and resources that you own or have explicit authorization to test.

---

## ✅ WEEK 3 PRACTICAL COMPLETED

**Modules Completed:**
- Module 1 – Password Cracking with John the Ripper
- Module 2 – Password Cracking with Networkwalks Tools

**Main Focus Areas:**
Password Cracking | Hash Extraction | Hash Analysis | Password Recovery | Cybersecurity | Ethical Hacking
