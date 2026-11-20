# 🔐 WEEK 3 – PASSWORD CRACKING PRACTICAL
### Cybersecurity & Ethical Hacking | Password Security and Hash Analysis[cite: 2, 10]

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-blue?style=for-the-badge)
![Week](https://img.shields.io/badge/Week-03-purple?style=for-the-badge)
![Practical](https://img.shields.io/badge/Practical-Completed-success?style=for-the-badge)
![Tools](https://img.shields.io/badge/Tools-JTR%20%7C%20Networkwalks-orange?style=for-the-badge)

---

# 📌 PROJECT OVERVIEW

This repository contains the lab report and documentation for the Week 3 Cybersecurity and Ethical Hacking practical exercises[cite: 2, 10].

The exercises focused on password cracking, password hash extraction, and password recovery from encrypted PDF documents[cite: 3, 11].

Two practical modules were completed using different password-cracking approaches[cite: 3, 11]:

- **Project Module 1:** Password Cracking with John the Ripper (JTR) and Johnny GUI.
- **Project Module 2:** Password Cracking with Networkwalks Tools.

For Module 1, three separate password-protected PDF documents were processed using John the Ripper[cite: 11]. Each document produced an individual password-cracking result.

Module 2 introduced the use of Networkwalks online tools to extract PDF password hashes and attempt password recovery[cite: 3].

The practical exercises provided hands-on experience with password security, hash extraction, and the importance of strong password protection[cite: 3, 11].

---

# 🎯 PROJECT OBJECTIVES

The objectives of these practical exercises were to:

- Understand password cracking and password hashing[cite: 3, 8].
- Identify how password-protected PDF documents are secured[cite: 3, 11].
- Extract password hashes from encrypted PDF files[cite: 3].
- Configure Johnny GUI and use John the Ripper to perform password-cracking attacks[cite: 11, 13, 14, 20].
- Use Networkwalks tools to extract and crack PDF hashes[cite: 3, 6].
- Verify recovered passwords by opening protected PDF documents[cite: 7, 8, 22, 23].
- Understand the importance of strong and unique passwords[cite: 3, 8, 11].

---

# 🛠️ TOOLS AND TECHNOLOGIES

| Tool | Purpose |
|---|---|
| John the Ripper | Password-cracking software[cite: 11] |
| Johnny GUI | Graphical interface for John the Ripper[cite: 11] |
| PDF Hash Extractor | Extracts hashes from protected PDF documents[cite: 15, 16] |
| Notepad | Saves extracted hash values[cite: 17, 18] |
| Networkwalks Hash Calculator | Generates PDF password hashes[cite: 3, 4, 5] |
| Networkwalks Password Cracker | Attempts password recovery[cite: 3, 6, 7] |
| Windows PC | Operating environment[cite: 3, 11] |
| Web Browser | Accesses online tools[cite: 3, 4, 6] |

## 🔗 TOOL REFERENCES

- [John the Ripper Official Website](https://www.openwall.com/john/)[cite: 12]
- [Johnny GUI](https://openwall.info/wiki/john/johnny)[cite: 12]
- [Online PDF Hash Extractor](https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php)[cite: 15, 16]
- [Networkwalks Practical Lab](https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/)[cite: 4]
- [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)[cite: 4]
- [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)[cite: 5, 6]

---

# 🔵 PROJECT MODULE 1: PASSWORD CRACKING WITH JOHN THE RIPPER

## 1.1 Background

John the Ripper (JTR) is a password-cracking tool commonly used by cybersecurity professionals to evaluate password strength[cite: 11].

It supports different password hash formats and can be used to test the security of password-protected files, including PDF documents[cite: 11].

Johnny is the graphical user interface for John the Ripper[cite: 11]. It provides a more accessible way to interact with JTR without relying entirely on command-line instructions[cite: 11].

This practical involved using both John the Ripper and Johnny GUI to recover passwords from three separate protected PDF documents[cite: 11].

## 1.2 Task

Use John the Ripper and Johnny GUI on a Windows PC to crack the passwords of three protected PDF documents[cite: 11]:

1. lockedpdf1
2. lockedpdf2
3. lockedpdf3

Each document was processed separately, and the results were documented individually.

---

## 1.3 PROCEDURE AND IMPLEMENTATION

### STEP 1 – Configure Johnny GUI

Johnny was opened[cite: 13].

The settings option was selected to configure the application and locate the John the Ripper executable[cite: 13].

The `john.exe` file was located inside the `run` folder within the John the Ripper directory[cite: 14].

The executable was selected to allow Johnny to communicate with John the Ripper[cite: 14].

**Screenshot 1 – Johnny GUI Opened**

![Johnny Interface](screenshots/JTR/01-johnny-interface.png)

**Screenshot 2 – Johnny Settings**

![Johnny Settings](screenshots/JTR/02-johnny-settings.png)

**Screenshot 3 – Locating john.exe**

![Locate John Executable](screenshots/JTR/03-locate-john-exe.png)

**Screenshot 4 – John Executable Selected**

![John Executable Selected](screenshots/JTR/04-john-exe-selected.png)

---

### STEP 2 – Prepare the Protected PDF Documents

Three password-protected PDF documents were used for the exercise[cite: 11].

The documents were prepared locally before beginning the hash extraction process[cite: 15, 22].

**Screenshot 5 – First Protected PDF**

![Locked PDF 1](screenshots/JTR/05-lockedpdf1.png)

**Screenshot 6 – Second Protected PDF**

![Locked PDF 2](screenshots/JTR/06-lockedpdf2.png)

**Screenshot 7 – Third Protected PDF**

![Locked PDF 3](screenshots/JTR/07-lockedpdf3.png)

---

### STEP 3 – Extract the PDF Password Hashes

The Online PDF Hash Extractor was accessed through a web browser[cite: 15].

Each protected PDF document was uploaded individually to extract its corresponding password hash[cite: 15, 16].

The extracted hash values were copied for use in John the Ripper[cite: 16].

The hash values were expected to begin with `$pdf$`[cite: 16].

**Screenshot 8 – PDF Hash Extractor Website**

![PDF Hash Extractor](screenshots/JTR/08-pdf-hash-extractor.png)

**Screenshot 9 – Uploading lockedpdf1**

![Upload PDF 1](screenshots/JTR/09-upload-lockedpdf1.png)

**Screenshot 10 – Hash Extracted for lockedpdf1**

![Hash PDF 1](screenshots/JTR/10-hash-lockedpdf1.png)

**Screenshot 11 – Hash Extracted for lockedpdf2**

![Hash PDF 2](screenshots/JTR/11-hash-lockedpdf2.png)

**Screenshot 12 – Hash Extracted for lockedpdf3**

![Hash PDF 3](screenshots/JTR/12-hash-lockedpdf3.png)

**Note:** If the extracted hash contains additional characters such as `b'` at the beginning, these should be removed before saving the hash file[cite: 16]. The hash should retain the correct `$pdf$` format[cite: 16].

---

### STEP 4 – Save the Extracted Hash Values

Notepad was opened to store the extracted hash values[cite: 17].

Each hash was saved in a text file for use in the cracking process[cite: 16, 17, 18].

The first hash file was saved as `hash1.txt`[cite: 18]. Separate files were prepared for the other PDF documents to keep the results organized.

**Screenshot 13 – Hash Pasted into Notepad**

![Hash in Notepad](screenshots/JTR/13-hash-notepad.png)

**Screenshot 14 – Saving Hash1.txt**

![Save Hash 1](screenshots/JTR/14-save-hash1.png)

**Screenshot 15 – Saving Hash2.txt**

![Save Hash 2](screenshots/JTR/15-save-hash2.png)

**Screenshot 16 – Saving Hash3.txt**

![Save Hash 3](screenshots/JTR/16-save-hash3.png)

---

### STEP 5 – Import Hash Files into Johnny

Johnny was reopened[cite: 18].

The Open Password File option was selected, and the saved hash text file was imported[cite: 19, 20].

This process was repeated for each of the three PDF documents.

**Screenshot 17 – Open Password File**

![Open Password File](screenshots/JTR/17-open-password-file.png)

**Screenshot 18 – Importing lockedpdf1 Hash**

![Import Hash 1](screenshots/JTR/18-import-hash1.png)

**Screenshot 19 – Importing lockedpdf2 Hash**

![Import Hash 2](screenshots/JTR/19-import-hash2.png)

**Screenshot 20 – Importing lockedpdf3 Hash**

![Import Hash 3](screenshots/JTR/20-import-hash3.png)

---

### STEP 6 – Start the Password-Cracking Attack

After importing each hash file, the Start New Attack option was selected[cite: 20].

John the Ripper began processing the hash and attempting to recover the corresponding password[cite: 20, 21].

The process was performed separately for each PDF document.

The time required depended on the computer's processing speed and the complexity of the password[cite: 20].

**Screenshot 21 – Starting Attack on lockedpdf1**

![Start Attack 1](screenshots/JTR/21-start-attack1.png)

**Screenshot 22 – Starting Attack on lockedpdf2**

![Start Attack 2](screenshots/JTR/22-start-attack2.png)

**Screenshot 23 – Starting Attack on lockedpdf3**

![Start Attack 3](screenshots/JTR/23-start-attack3.png)

---

## 1.4 RESULTS AND SCREENSHOTS

The three protected PDF documents were processed individually using John the Ripper[cite: 11].

Each document produced a different password-cracking result.

The screenshots below provide placeholders for the individual results obtained during the practical.

### RESULT 1 – lockedpdf1

**Description:** Password-cracking result for the first protected PDF document[cite: 11].

**Screenshot:**

![lockedpdf1 Cracking Result](screenshots/JTR/24-lockedpdf1-result.png)

**PDF Verification:**

![lockedpdf1 Opened](screenshots/JTR/25-lockedpdf1-verified.png)

---

### RESULT 2 – lockedpdf2

**Description:** Password-cracking result for the second protected PDF document.

**Screenshot:**

![lockedpdf2 Cracking Result](screenshots/JTR/26-lockedpdf2-result.png)

**PDF Verification:**

![lockedpdf2 Opened](screenshots/JTR/27-lockedpdf2-verified.png)

---

### RESULT 3 – lockedpdf3

**Description:** Password-cracking result for the third protected PDF document.

**Screenshot:**

![lockedpdf3 Cracking Result](screenshots/JTR/28-lockedpdf3-result.png)

**PDF Verification:**

![lockedpdf3 Opened](screenshots/JTR/29-lockedpdf3-verified.png)

---

## 1.5 MODULE 1 SUMMARY

The first module provided practical experience using John the Ripper and Johnny GUI to recover passwords from encrypted PDF documents[cite: 11].

Three separate PDF files were processed, with individual hash extraction, import, cracking, and result verification.

The exercise demonstrated how password hashes can be extracted and used in password-cracking tools to evaluate the strength of document passwords[cite: 11].

---

# 🟣 PROJECT MODULE 2: PASSWORD CRACKING WITH NETWORKWALKS TOOLS

## 2.1 Background

The second practical exercise focused on using Networkwalks online tools to extract and crack passwords from protected PDF documents[cite: 3].

The exercise involved two main tools[cite: 3]:

- Networkwalks Hash Calculator[cite: 3, 4]
- Networkwalks Password Cracker[cite: 3, 5, 6]

These tools were accessed directly through a web browser[cite: 3].

The Hash Calculator was used to generate the PDF password hash, while the Password Cracker attempted to recover the original password from that hash[cite: 3, 5, 6].

## 2.2 Task

Use the Networkwalks Hash Calculator and Password Cracker tools on a Windows laptop to recover the password of the provided protected PDF document[cite: 3].

---

## 2.3 PROCEDURE AND IMPLEMENTATION

### STEP 1 – Access the Encrypted PDF

The Networkwalks practical lab resources were accessed[cite: 4, 30].

The protected PDF document, identified in the lab instructions as `My Locked PDF1.pdf`, was opened for analysis[cite: 4, 30].

**Screenshot 1 – Networkwalks Lab Page**

![Networkwalks Lab](screenshots/Networkwalks/01-networkwalks-lab.png)

**Screenshot 2 – Protected PDF (`My Locked PDF1.pdf`)**

![Protected PDF](screenshots/Networkwalks/02-downloaded-pdf.png)[cite: 30]

---

### STEP 2 – Open the Networkwalks Hash Calculator

The Networkwalks Hash Calculator was opened using the web browser[cite: 4, 29].

The tool was prepared to receive the protected PDF document[cite: 4, 29].

**Screenshot 3 – Hash Calculator Website**

![Hash Calculator](screenshots/Networkwalks/03-hash-calculator.png)[cite: 29]

---

### STEP 3 – Upload the Protected PDF

The protected PDF document was uploaded to the Hash Calculator[cite: 4, 5, 28].

The tool processed the file and generated its corresponding PDF password hash[cite: 4, 5, 28].

**Screenshot 4 – Selecting the PDF File**

![Select PDF](screenshots/Networkwalks/04-select-pdf.png)

**Screenshot 5 – PDF Uploaded**

![PDF Uploaded](screenshots/Networkwalks/05-pdf-uploaded.png)

---

### STEP 4 – Copy the Extracted Hash

After the file was processed, the generated hash was displayed[cite: 5, 28].

The complete hash value was copied for use in the Password Cracker[cite: 5, 6].

The hash began with `$pdf$`[cite: 4, 5, 28].

**Screenshot 6 – Generated PDF Hash (`My-Locked-PDF1.pdf`)**

![Generated Hash](screenshots/Networkwalks/06-generated-hash.png)[cite: 28]

**Screenshot 7 – Copying the Complete Hash**

![Copy Hash](screenshots/Networkwalks/07-copy-hash.png)

---

### STEP 5 – Open the Networkwalks Password Cracker

The Networkwalks Password Cracker was accessed through the web browser[cite: 5, 6, 31].

The tool was prepared to receive the extracted hash value[cite: 6, 31].

**Screenshot 8 – Password Cracker Website**

![Password Cracker](screenshots/Networkwalks/08-password-cracker.png)[cite: 31]

---

### STEP 6 – Submit the Hash and Start the Attack

The copied PDF hash was pasted into the Password Cracker[cite: 6, 27].

The Start Attack option was selected to begin the password-recovery process[cite: 6, 26].

The tool attempted different password combinations until a match was found or the attempt concluded[cite: 6, 7, 26].

**Screenshot 9 – Hash Entered into Password Cracker**

![Hash Entered](screenshots/Networkwalks/09-hash-entered.png)[cite: 27]

**Screenshot 10 – Password-Cracking Process Started (58% Progress)**

![Attack Started](screenshots/Networkwalks/10-attack-started.png)[cite: 26]

---

### STEP 7 – Review the Cracking Result

The Password Cracker was allowed to complete its process[cite: 7, 25].

The result displayed by the tool was reviewed — `password1` was matched[cite: 7, 25].

The time taken depended on the complexity of the password[cite: 7].

**Screenshot 11 – Password-Cracking Result (`password1` Cracked)**

![Cracking Result](screenshots/Networkwalks/11-cracking-result.png)[cite: 25]

---

### STEP 8 – Verify the Recovered Password

The protected PDF document was opened[cite: 7, 8, 24].

The recovered password (`password1`) was entered to confirm that the document could be accessed successfully, revealing Flag 1: `nw{networkwalks_flag1_jtr_270521_1}`[cite: 7, 8, 24].

**Screenshot 12 – Entering the Recovered Password**

![Enter Password](screenshots/Networkwalks/12-enter-password.png)

**Screenshot 13 – Successfully Opened PDF & Captured Flag (`nw{networkwalks_flag1_jtr_270521_1}`)**

![PDF Opened](screenshots/Networkwalks/13-pdf-opened.png)[cite: 24]

---

## 2.4 MODULE 2 SUMMARY

The second module demonstrated how Networkwalks online tools can be used to extract PDF password hashes and attempt password recovery[cite: 3].

The Hash Calculator generated the hash (`$pdf$...`), which was then submitted to the Password Cracker[cite: 3, 4, 6, 28].

The recovered password (`password1`) was tested against the protected PDF document to verify the result and capture Flag 1 (`nw{networkwalks_flag1_jtr_270521_1}`)[cite: 7, 8, 24].

This exercise provided additional insight into password cracking using browser-based cybersecurity tools[cite: 3].

---

# 📚 KEY LEARNINGS

The Week 3 practical exercises provided hands-on experience in password security and password-cracking techniques[cite: 3, 11].

The main lessons learned include:

### 1. Password Hashing
Developed an understanding of how passwords are represented through cryptographic hashes[cite: 3, 8].

### 2. Hash Extraction
Learned how to extract password hashes from encrypted PDF documents using online tools[cite: 3, 4, 15].

### 3. John the Ripper
Gained practical experience configuring and using John the Ripper with Johnny GUI[cite: 11, 13, 14].

### 4. Password Cracking
Learned how password-cracking tools process hashes and attempt to identify the original password[cite: 3, 6, 7, 20, 21].

### 5. Networkwalks Tools
Gained experience using online tools to calculate PDF hashes and attempt password recovery[cite: 3, 4, 6, 7].

### 6. Password Verification
Understood the importance of testing recovered passwords against the original protected documents[cite: 7, 8, 22, 23].

### 7. Password Security
Recognized the importance of strong, unique, and complex passwords in protecting sensitive information[cite: 3, 8, 11].

---

# 🔒 SECURITY RECOMMENDATIONS

Based on the exercises completed, the following security practices are recommended:

- Use long and complex passwords[cite: 8].
- Avoid common words and predictable password combinations[cite: 3, 8].
- Use unique passwords for different accounts and documents.
- Consider using a reputable password manager.
- Protect sensitive documents with strong encryption[cite: 8].
- Avoid sharing passwords and password hashes with unauthorized individuals.
- Use multi-factor authentication where available.
- Regularly review password security practices.

---

# 📝 CONCLUSION

The Week 3 practical exercises provided valuable hands-on experience in password cracking, hash extraction, and password security[cite: 3, 11].

The first module focused on using John the Ripper and Johnny GUI to process three separate password-protected PDF documents[cite: 11]. Each document was handled individually, producing three different password-cracking results.

The second module introduced Networkwalks online tools, demonstrating how PDF password hashes can be extracted and submitted for password recovery[cite: 3].

Overall, the exercises strengthened my understanding of password protection, hash analysis, and the methods used by cybersecurity professionals to evaluate password security[cite: 3, 11].

The practical activities also highlighted the importance of creating strong passwords to reduce the risk of unauthorized access[cite: 3, 8, 11].

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
│   │   ├── 01-johnny-interface.png
│   │   ├── 02-johnny-settings.png
│   │   ├── 03-locate-john-exe.png
│   │   ├── 04-john-exe-selected.png
│   │   ├── 05-lockedpdf1.png
│   │   ├── 06-lockedpdf2.png
│   │   ├── 07-lockedpdf3.png
│   │   ├── 08-pdf-hash-extractor.png
│   │   ├── 09-upload-lockedpdf1.png
│   │   ├── 10-hash-lockedpdf1.png
│   │   ├── 11-hash-lockedpdf2.png
│   │   ├── 12-hash-lockedpdf3.png
│   │   ├── 13-hash-notepad.png
│   │   ├── 14-save-hash1.png
│   │   ├── 15-save-hash2.png
│   │   ├── 16-save-hash3.png
│   │   ├── 17-open-password-file.png
│   │   ├── 18-import-hash1.png
│   │   ├── 19-import-hash2.png
│   │   ├── 20-import-hash3.png
│   │   ├── 21-start-attack1.png
│   │   ├── 22-start-attack2.png
│   │   ├── 23-start-attack3.png
│   │   ├── 24-lockedpdf1-result.png
│   │   ├── 25-lockedpdf1-verified.png
│   │   ├── 26-lockedpdf2-result.png
│   │   ├── 27-lockedpdf2-verified.png
│   │   ├── 28-lockedpdf3-result.png
│   │   └── 29-lockedpdf3-verified.png
│   │
│   └── Networkwalks/
│       ├── 01-networkwalks-lab.png
│       ├── 02-downloaded-pdf.png       # password.jpeg
│       ├── 03-hash-calculator.png        # wait.jpeg
│       ├── 04-select-pdf.png
│       ├── 05-pdf-uploaded.png
│       ├── 06-generated-hash.png         # encryted.jpeg
│       ├── 07-copy-hash.png
│       ├── 08-password-cracker.png       # hash'.jpeg
│       ├── 09-hash-entered.png           # crac.jpeg
│       ├── 10-attack-started.png         # cracking.jpeg
│       ├── 11-cracking-result.png        # sucess.jpeg
│       ├── 12-enter-password.png
│       └── 13-pdf-opened.png             # flag 1.jpeg
│
└── documents/
    └── Practical-Reference-Materials/
