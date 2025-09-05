# Splunk-BruteForce-Detection

# Splunk Project: Brute Force Detection

# Project Idea
Detect brute-force login attempts using Splunk.

# Dataset
- Sample auth logs (sample_logs.csv)

# Splunk Query
```spl
index=auth_logs action=failure 
| stats count by src_ip, user 
| where count > 5
