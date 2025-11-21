#  SQL Security Analytics: Threat Detection & Employee Auditing

A cybersecurity investigation project using **advanced SQL filtering** to identify security threats and analyze internal systems.

##  Project Overview

This project demonstrates practical SQL applications in cybersecurity through analysis of login attempts and employee data. The investigation focuses on detecting suspicious patterns and generating actionable security insights.

## Technical Analysis

**Databases Used:**
- `log_in_attempts` - Authentication events and access patterns
- `employees` - Staff information and asset assignments

**Key Investigations:**

| Security Analysis | SQL Techniques | Business Impact |
|-------------------|----------------|-----------------|
| **After-Hours Failed Logins** | `WHERE` with time filters and boolean logic | Identify brute-force attacks outside business hours |
| **Suspicious Date-Based Activity** | `BETWEEN` for date ranges | Forensic analysis of specific incident periods |
| **International Login Attempts** | `NOT LIKE` for geographic exclusion | Detect potentially malicious foreign access |
| **Department-Specific Asset Audit** | `LIKE` with pattern matching | Inventory management and access control verification |
| **Multi-Department Employee Retrieval** | `OR` conditions | Cross-functional reporting and compliance |
| **Non-Technical Staff Filtering** | `NOT` operator | Target security awareness training |

##  Skills Demonstrated

- **Security-Focused SQL Querying**
- **Advanced Conditional Filtering** (`WHERE`, `AND`, `OR`, `NOT`)
- **Pattern Matching** (`LIKE`, `BETWEEN`)
- **Threat Detection & Analysis**
- **Data-Driven Security Insights**

## 📄 Documentation

[View Full Project Analysis][SQL_Filtering_Security_Investigation.doc.pdf](https://github.com/user-attachments/files/23683043/SQL_Filtering_Security_Investigation.doc.pdf)


## 👤 Author

**Muhammad Bilal**  
- 🔗 [LinkedIn](https://www.linkedin.com/in/muhammad-bilal-2089a532b)  
- 🐙 [GitHub](https://github.com/Muhammad-Bilal834)

---

*This project showcases practical SQL applications in cybersecurity contexts, demonstrating how database querying skills can be leveraged for real-world security monitoring and threat detection.*
