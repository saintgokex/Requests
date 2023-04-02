# Requests
A data visualization project, using SQL and Power BI to create interactive and informative charts and graphs from three different datasets: location report, service type report and request status report. The project includes detailed code documentation, examples of different visualization techniques, and a final dashboard or report.
# Request Status Report
This dataset explores the requests made by clients of a consultng firm, their location, service type and the request status. 
## Data Source
I came across three datasets namely; request status report, locatons report and service type report on a Data Analyst Whatsapp group. The first mentioned dataset contains the following observations: request number, quotaion amount, paid amount and request status, the second contains request number, province, lon and lat while the last contains request number and service type.
## Data Manipulation
I imported all the three datasets into SQL and joined them all using the code 
```  SELECT
 *	
FROM 
`learned-helper-378420.request.location_report` AS location_report
JOIN `learned-helper-378420.request.request_status` AS request_status
 ON location_report.Request_Number = request_status.Request_Number
JOIN `learned-helper-378420.request.service_type` AS service_type
 ON service_type.string_field_0 = location_report.Request_Number
![image](https://user-images.githubusercontent.com/110998224/229326105-c4051f53-4220-4a3a-8396-ffbac82a62c4.png)
```
## Data Cleaning
1. Saved new table
2. Imported new Table to google sheets
3. Created new column "month" using the function “=TEXT(B2, “MMMM”)” 
4. Deleted duplicates
5. Saved and imported file into Power BI for analysis and visualization
## Data Analysis and Visualization
### Dashboard
! [ ] (https://github.com/saintgokex/Requests/blob/main/dashboard.png)
## Results
