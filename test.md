Certainly, here's an improved version of the architecture with clearer descriptions and formatting:

1. **Fetch Unscanned Reports from Wiz and Store in S3 Bucket**
   - Implement a Lambda Function to retrieve unscanned reports from Wiz.
   - Store these reports securely in an S3 bucket.

2. **Retrieve CMDB Details and Store in S3**
   - Develop a process to fetch CMDB (Configuration Management Database) details.
   - Save this information in an S3 bucket alongside the reports.

3. **Submit Adhoc Requests Using SNOW API**
   - Utilize the ServiceNow (SNOW) API to submit adhoc requests with the following details:
     a) Account email (retrieved from CMDB).
     b) Description (extracted from Wiz reports).
     c) Title for the request.

4. **Send Advanced Email Notifications**
   - Send advanced email notifications to our team, 6 hours before raising the SNOW requests.
   - Include the ticket details in the email and create a reference file.

5. **Monitor SNOW Request Status**
   - Continuously monitor the status of the SNOW requests for existing tickets.

6. **Open New Requests for Closed Tickets**
   - If a ticket is marked as closed in SNOW, open a new request as needed.
   - In case a new entry is found on the same cloud account, raise another SNOW ticket accordingly.

7. **Handle Special Cases with Exceptions**
   - Implement a mechanism to handle special cases and exceptions.
   - Customize the process based on specific conditions.

8. **Scheduled Cloud Account Checks**
   - Periodically, check the cloud account for updates and run the entire process as needed.

This revised architecture provides a more organized and detailed overview of your system's workflow for fetching, processing, and managing requests, as well as handling various scenarios and exceptions.
