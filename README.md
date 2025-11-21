# SQL Security Analytics: Threat Detection and Employee Auditing

A comprehensive cybersecurity investigation project utilizing advanced SQL filtering techniques to identify security threats, analyze suspicious activities, and manage enterprise asset allocations.

## Project Overview

This project demonstrates practical SQL applications in cybersecurity operations. As part of organizational security enhancement initiatives, I conducted systematic analysis of login patterns and employee machine management using advanced database querying techniques to strengthen system security and streamline IT operations.

## Technologies Used
- **Database**: MySQL
- **Tools**: MySQL Workbench / Command Line Interface
- **Analysis**: Security-focused SQL querying and filtering
- **Focus**: Threat detection, employee asset management, security auditing

## Security Investigations

### After-Hours Failed Login Attempts
**Objective:** Identify potential brute-force attacks occurring outside business hours (after 18:00)
```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
```

### Login Attempts on Specific Dates  
**Objective:** Investigate suspicious activity during targeted timeframes (2022-05-08 to 2022-05-09)
```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

### Login Attempts Outside of Mexico
**Objective:** Detect potentially malicious access from unauthorized geographic locations
```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

## Employee Machine Management

### Marketing Department (East Building)
**Objective:** Retrieve employee machines for targeted security updates in specific department/location
```sql
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

### Finance or Sales Departments
**Objective:** Coordinate security updates across multiple business departments
```sql
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';
```

### Non-IT Employees
**Objective:** Manage security updates for non-technical staff requiring different protocols
```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

## Database Schema
```sql
-- log_in_attempts table structure
CREATE TABLE log_in_attempts (
    event_id INT,
    username VARCHAR(50),
    login_date DATE,
    login_time TIME,
    country VARCHAR(50),
    ip_address VARCHAR(15),
    success BOOLEAN
);

-- employees table structure  
CREATE TABLE employees (
    employee_id INT,
    device_id VARCHAR(50),
    username VARCHAR(50),
    department VARCHAR(50),
    office VARCHAR(50)
);
```

## Key Findings and Impact

### Security Enhancements
- Identified multiple suspicious login patterns including after-hours failed attempts and unauthorized geographic access
- Improved threat detection capabilities through systematic login analysis
- Enhanced monitoring protocols for abnormal authentication activities

### Operational Efficiency  
- Streamlined security updates for employee machines across multiple departments
- Enabled targeted asset management through department-specific filtering
- Automated employee machine auditing processes

### Technical Achievements
- Demonstrated practical SQL applications in real-world cybersecurity scenarios
- Implemented complex filtering logic for precise data retrieval
- Established repeatable analysis frameworks for ongoing security monitoring

## Skills Demonstrated

- **Security-Focused SQL Querying** - Threat detection through data analysis
- **Advanced Conditional Filtering** - WHERE, AND, OR, NOT operators
- **Pattern Matching and Wildcards** - LIKE with % for flexible searching
- **Data-Driven Decision Making** - Translating query results into actionable insights
- **Cybersecurity Fundamentals** - Authentication monitoring and access control
- **Database Management** - Schema understanding and optimized query design

## Project Documentation

[View Full Project Analysis and Queries][SQL_Filtering_Security_Investigation.doc.pdf](https://github.com/user-attachments/files/23683233/SQL_Filtering_Security_Investigation.doc.pdf)


## Author

**Muhammad Bilal**  
Cybersecurity Enthusiast | Data Analyst | SQL Specialist

- LinkedIn: https://www.linkedin.com/in/muhammad-bilal-2089a532b
- GitHub: https://github.com/Muhammad-Bilal834

---

This project showcases the critical role of SQL in modern cybersecurity operations, demonstrating how targeted database analysis can identify threats, streamline operations, and enhance organizational security posture through data-driven insights.
