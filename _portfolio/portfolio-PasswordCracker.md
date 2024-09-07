---
title: "Password Cracker"
excerpt: "The project’s goal was to developed a website to crack and validate the password using MD5 of registered users and validate the password as strong, moderate, and weak. To do so a list of 2000 commonly used passwords was used and tested using permutations with 0-9 digits and special characters. To optimize, the password was restricted to use at most 2 numbers and 2 special characters. [![Password Cracker](https://navoditamathur.github.io/files/password-cracking.jpg)](https://navoditamathur.github.io/portfolio/portfolio-PasswordCracker)"
collection: portfolio
tags: 
  - password cracking
---

Introduction:
------
In the realm of information technology, data security is paramount. It involves implementing strategies to protect digital information from unauthorized access, ensuring that sensitive data remains confidential and secure. A key component of data security is the use of strong passwords. Passwords serve as the first line of defense in safeguarding personal and sensitive information across various online platforms, devices, and networks. This project demonstrates the importance of strong password practices and the vulnerabilities of weak passwords.

Objective:
------
The primary objective of this project was to develop a web application that allows users to register, log in, and validate the strength of their passwords. Additionally, the application includes a password-cracking feature that evaluates the strength of user passwords by testing them against a dictionary of commonly used passwords, with the goal of educating users about password security.

Description:
------
The project consists of several key features:

- User Registration and Password Storage:
The application allows users to register by providing a username and password. For security, the system stores only the MD5 hash of the password rather than the password itself. The password is restricted to lowercase letters, with a maximum of two numbers and two special characters ('@', '#', '$', '%', '&').

- User Login and Authentication:
Registered users can log in by entering their username and password. The system computes the MD5 hash of the entered password and compares it with the stored hash. Users are granted access only if the hashes match.

- Password Cracking Mechanism:
The application includes a feature to crack passwords based on a dictionary of 2,000 commonly used passwords. This feature tests permutations of these passwords by adding digits and special characters to simulate common password patterns.

![Password Cracker](https://navoditamathur.github.io/files/password-cracked.png)

- Password Validation:
Users can validate the strength of their passwords within the application. The system assesses how long it would take to crack the password based on its complexity and provides feedback on whether the password is strong, moderate, or weak.

![Password Validator](https://navoditamathur.github.io/files/password_validated.png)

- Read More [here](https://navoditamathur.github.io/files/nam266_ProjectReport.pdf)

Methodology:
------
- Password Hashing: MD5 hashing is used to store passwords securely. This prevents attackers from easily retrieving the original password if the system is compromised.
- Dictionary-Based Cracking: The cracking mechanism uses a dictionary of common passwords, enhancing its effectiveness by applying permutations with digits and special characters to simulate real-world password-guessing strategies.
- Optimization: To ensure a balance between security and usability, the system restricts passwords to a maximum of two numbers and two special characters, reducing the processing time for cracking while encouraging users to create sufficiently complex passwords.

Deliverables:
------
Web Application: A fully functional [web application](https://nam266.pythonanywhere.com/) with features for user registration, login, password cracking, and validation.

Conclusion:
------
The Password Cracker project underscores the importance of strong password practices in safeguarding sensitive information. By providing users with tools to test and validate their passwords, this project contributes to raising awareness about password security and the vulnerabilities associated with weak passwords. The use of MD5 hashing, combined with a dictionary-based cracking mechanism, offers a practical demonstration of common security challenges and the importance of using complex, unique passwords
