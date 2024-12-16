#### What is Observability Tool ?

It gives Internal state of systme where your app is established with infrastructure and networks.

Ex. What was Disk Utilizations of particular node or nodes for last 24 hr ?

What was cpu utilizations for 24 hr ?

How many http request are success and failed for last 20 minutes ?

#### Observability can help into understood

- what is the issues in your application ?

- Why that issue was happens ? 

- What is the reason of failure or fail 5 http request ?

- How to fix that issues, gives solutions

##### what is the piller of Observability ?

1. #### ```Metrics```
    -  Data Metrics like Http Request, CPU , Memory etc.
    - Metrics gives you historical data.

2. #### ```Logging``` 
    - You can get log details for when, why that your metrics get fails.

3. #### ```Traces``` 
    -  It will Trace your metrics like 5 out of 100 https was fails.
    - What was exactly happens with 5 http request from user requested to reach your infrastructure setup
    - which case , which infrastructure part that http request did not receive or fails.

#### 🖥️ What Can Be Monitored?
- Infrastructure: CPU usage, memory usage, disk I/O, network traffic.
- Applications: Response times, error rates, throughput.
- Databases: Query performance, connection pool usage, transaction rates.
- Network: Latency, packet loss, bandwidth usage.
- Security: Unauthorized access attempts, vulnerability scans, firewall logs.

#### 👀 What Can Be Observed?
- Logs: Detailed records of events and transactions within the system.
- Metrics: Quantitative data points like CPU load, memory consumption, and request counts.
- Traces: Data that shows the flow of requests through various services and components.
