Log Analysis with Python
This project analyzes web server logs to extract key insights, including the number of requests per IP, the most accessed endpoints, and suspicious activities like excessive failed login attempts.

Features
1. Requests per IP
Displays the number of requests made by each IP address.
Example Output:

IP Address           Request Count  
192.168.1.1          69  
203.0.113.5          8  
198.51.100.23        8  
10.0.0.2             6  
192.168.1.100        5  
2. Most Accessed Endpoint
Identifies the most frequently accessed endpoint in the log data.
Example Output:

Most Frequently Accessed Endpoint:  
/ home (Accessed 67 times)  
3. Suspicious Activity Detection
Flags IP addresses with excessive failed login attempts, indicating possible suspicious behavior.

Example Output:

Suspicious Activity Detected:  
No suspicious activity detected.  
How It Works
Log Parsing:

Extracts IP addresses, HTTP methods, status codes, and endpoints using regular expressions.
Analysis:

Counts requests per IP.
Determines the most accessed endpoint.
Identifies IPs with failed login attempts exceeding a defined threshold.
Output:

Displays results in the terminal.
Saves the analyzed data to a CSV file for easy access.
Usage
Clone this repository and place the log file (sample.log) in the same directory.
Run the script:
python log_analysis.py  
View the results in the terminal and the generated log_analysis_results.csv file.
Sample Input
A snippet from the input log file (sample.log):

192.168.1.1 - - [03/Dec/2024:10:12:34 +0000] "GET /home HTTP/1.1" 200 512  
203.0.113.5 - - [03/Dec/2024:10:12:35 +0000] "POST /login HTTP/1.1" 401 128 "Invalid credentials"  
10.0.0.2 - - [03/Dec/2024:10:12:36 +0000] "GET /about HTTP/1.1" 200 256  
Results
Requests per IP Address
Most Frequently Accessed Endpoint
Suspicious Activity
CSV Output
Results are saved in log_analysis_results.csv for detailed inspection.

