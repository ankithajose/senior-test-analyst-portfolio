This folder demonstrates my approach to API testing using Postman, with a strong focus on manual validation, negative testing, and backend data quality risks.
The examples reflect how I test APIs in real-world Agile environments, going beyond happy-path scenarios to identify validation gaps and business risks.

The Postman collection in this folder includes:
Positive API scenarios (valid requests)
Negative API testing, including:
Empty request body
Missing mandatory fields
Invalid data formats (e.g. email validation)
HTTP status code validation
Response structure verification
Data integrity and backend validation checks

These tests are designed to validate not just API responses, but whether business rules and data constraints are enforced at the API layer.

Test Result:
During negative testing, the API returned 201 Created responses for:

Empty request payloads
Requests missing mandatory fields
Invalid email formats
This highlights a server-side validation gap, where the backend allows creation of incomplete or invalid records. Such behaviour can lead to data integrity issues, inconsistent user experiences, and downstream integration risks.

This folder intentionally documents these outcomes to demonstrate:

Risk-based testing mindset
Ability to challenge expected vs actual behaviour
Focus on quality beyond “green responses”

Tools & Techniques Used
Postman for API testing
Manual & exploratory testing
Positive testing techinques
Negative testing techniques
Risk-based testing approach
Environment variables for base URL and tokens
Clear test case separation (one request = one scenario)
