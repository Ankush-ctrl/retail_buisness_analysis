# retail_buisness_analysis
# workflow ~ 
             1. Data understanding 
             2. Data-quality assessment 
             3. Primary and foreign key validation
             4. Data cleaning
             5. SQL database design and analysis
             6. Power BI dashboard
             7. Business insights and recommendations

# what's going on 1-4 steps:
a. Loaded 6 CSV files and inspected their structure using info(), describe() and shape ~
| Dataset | Records | Columns |
| :--- | :---: | :---: |
| Customers | 15,266 | 10 |
| Products | 2,517 | 10 |
| Sales | 62,884 | 9 |
| Stores | 67 | 5 |
| Exchange Rates | 11,215 | 3 |
| Data Dictionary | 37 | 3 |

b. We found three issues:
| Dataset | Column | Missing Records | Decision | Reason |
| :--- | :--- | :---: | :--- | :--- |
| **Customers** | State Code | 10 | Retain | No verified State Code mapping was available for Napoli. |
| **Sales** | Delivery Date | 49,719 | Retain | Missing Delivery Dates occur in physical-store transactions, suggesting they may not apply. |
| **Stores** | Square Meters | 1 | Retain | Missing Square Meters belongs to the online store. |

c. Reasons:
1) No verified State Code mapping was available for Napoli.
2) Missing Delivery Dates occur in physical-store transactions, suggesting they may not apply.
3) Missing Square Meters belongs to the online store.
