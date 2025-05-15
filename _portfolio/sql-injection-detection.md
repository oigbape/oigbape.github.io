---
title: "SQL Injection Detection and Prevention Model"
collection: portfolio
order: 8
excerpt: "Designed a hybrid signature-anomaly detection model to secure an academic institution's web portal, achieving 100% blocking of SQLi attacks. Implemented input sanitization, MD5 hashing, and automated IP blocking via .htaccess."
#date: 2023-05-01
tags: [Cybersecurity, PHP, SQL, Web Application Security, Intrusion Detection, Input Validation, Anomaly Detection]
technologies: "PHP, MySQL, Apache, Regular Expressions, .htaccess"
# github_url: "[Link to GitHub repo]"
# report_url: "/files/SQLi_Prevention_Report.pdf"
# image_path: "/images/portfolio/sqli-defense-teaser.png"
---

## Objective
To develop a robust defense system for Auchi Polytechnic's Student Information Management System, protecting sensitive academic data from SQL injection (SQLi) attacks through multi-layered detection, real-time query sanitization, and compliance with Nigeria's NITDA cybersecurity guidelines.

## My Role & Contributions
* Designed a **hybrid detection methodology** combining signature-based pattern matching (blacklist of 30+ SQLi keywords/symbols) and anomaly-based behavioral analysis (IP rate-limiting).
* Built input validation layers using PHP’s `mysql_real_escape_string()`, `strip_tags()`, and `stripslashes()` to sanitize user inputs.
* Implemented MD5 password hashing to secure credentials, ensuring encrypted storage even if databases were compromised.
* Automated IP blocking via `.htaccess` for repeat offenders, reducing unauthorized access attempts by 95% during testing.
* Tested against 30+ SQLi variants (e.g., UNION-based, blind SQLi, hex-encoded payloads), achieving 100% detection/blocking accuracy.
* Collaborated with administrators to deploy the system, integrating it into the institution’s academic web portal.

## Technologies Used
* **Programming Languages:** PHP, SQL
* **Databases:** MySQL (user/attack logging)
* **Web Server:** Apache (IP blocking via `.htaccess`)
* **Security Tools:** Regular Expressions (pattern matching), MD5 hashing

## Key Outcomes & Achievements
* Deployed as part of Auchi Polytechnic’s production environment, enhancing compliance with national cybersecurity standards.
* Successfully blocked all tested SQLi attack vectors during evaluation, including high-risk payloads like `' OR 1=1--` and `10; DROP TABLE users`.
* Reduced fraudulent login attempts by 95% through automated IP blocking and behavioral rate-limiting.
* Provided administrators with a real-time monitoring interface for attack analytics and manual IP management.

## Artifacts
* **Project Report:** [Link to PDF if available](#)
* **GitHub Repository:** [Link to code if public](#)
