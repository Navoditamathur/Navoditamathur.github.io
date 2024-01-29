---
title: "Password Cracker"
excerpt: "The project’s goal was to developed a website to crack and validate the password using MD5 of registered users and validate the password as strong, moderate, and weak. To do so a list of 2000 commonly used passwords was used and tested using permutations with 0-9 digits and special characters. To optimize, the password was restricted to use at most 2 numbers and 2 special characters"
collection: portfolio
---

Introduction
-------
Data security is a critical aspect of information technology and involves implementing measures to protect digital information from unauthorized access, disclosure, alteration, or destruction. Ensuring data security is essential for safeguarding sensitive information and maintaining the trust of individuals, businesses, and organizations. Here are key components and best practices related to data security:

* Encryption:
  * Use encryption algorithms to convert sensitive data into unreadable format, and only authorized parties with the decryption key can access the original information.
  * Implement end-to-end encryption for communication channels to secure data during transmission.
  
* Access Control:
  * Enforce strict access controls to limit access to data based on user roles and permissions.
  * Authenticate users with strong authentication mechanisms, such as multi-factor authentication (MFA).
  
* Regular Auditing and Monitoring:
  * Conduct regular audits to track data access and changes.
  * Implement real-time monitoring systems to detect and respond to suspicious activities promptly.
  
* Data Backup and Recovery:
  * Regularly back up critical data to ensure its availability in case of data loss or system failures.
  * Develop and test a robust data recovery plan to minimize downtime and data loss.

Passwords are a common form of authentication and are designed to verify the identity of the person trying to access the system. They are often required to be kept confidential and are a crucial component of securing personal and sensitive information in various online platforms, devices, or networks. Hence it is important to use strong passwords. The more unique the password is, the more difficult it is to crack.

This is a small demo to demonstrate this

Description:
-------
The project has a mechanism that registers and adds a new user into the system and stores the user’s password information in a file. The password can contain only lowercase letters and a maximum of 2 numbers and 2 special characters ('@', '#', '$', '%', '&'). Security is ensured by storing not the password strings but message digests (hash) of the passwords to prevent attacks. It also allows registered users to login using a module which asks for the username and password from the user and verifies it based on the information stored in the password file. It computes the MD5 message digest of the entered password and checks if it matches the MD5 digest of the corresponding user password stored in the password file. The program accepts the user only if the message digests match.
The project also offers mechanisms to crack the password of any existing user with a known username based on a dictionary of commonly used words. Users logged in can also validate their passwords and know the time taken to crack their password and how strong it is.

The more uncommon a word is chosen as password, the harder it is to crack. Increase in complexity of passwords with the help of numbers and special characters, leads to increase in time and processing power required to crack the password.

Deliverables:
-------
A fully functional website to register, login, crack and validate passwords.