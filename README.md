# retail_buisness_analysis
# workflow ~ 
             1. Data understanding 
             2. Data-quality assessment 
             3. Primary and foreign key validation
             4. Data cleaning
             5. SQL database design and analysis
             6. Power BI dashboard
             7. Business insights and recommendations
1)
a. Loaded 6 CSV files and inspected their structure using info(), describe() and shap 
Dataset	            Records	     Columns
Customers          	15,266       	 10
Products	           2,517	       10
Sales	              62,884	        9
Stores	                67	        5
Exchange Rates	    11,215	        3
Data Dictionary	        37	        3

b. We found three issues:
Dataset	     Column	Missing           records	     Decision
Customers	     State Code             	10	        Retain
Sales	         Delivery Date	          49,719	    Retain
Stores	       Square Meters	          1	          Retain

c. Reasons:
- No verified State Code mapping was available for Napoli.
- Missing Delivery Dates occur in physical-store transactions, suggesting they may not apply.
- Missing Square Meters belongs to the online store.
