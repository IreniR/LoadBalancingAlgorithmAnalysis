# Load Balancing Performance Evaluation

## Overview

This project provides a comprehensive **implementation, evaluation, and comparison of static and dynamic load balancing algorithms**. It analyzes their performance in terms of **availability, scalability, response time, throughput, and security**, simulating realistic cloud workloads.

Deployed on both **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**, this project highlights the practical differences and effectiveness of these algorithms in real-world environments. The study provides actionable, data-driven insights for selecting the appropriate algorithm based on system requirements.

---

## Implemented Algorithms

### Static Load Balancing Algorithms
- **Round Robin**
- **IP Hash**

### Dynamic Load Balancing Algorithms
- **Least Connections**
- **Weighted Load Balancing**
- **Random**
- **Least Bandwidth**

---

## Cloud Deployment Details

### Amazon Web Services (AWS)
- Deployed backend services on **EC2 instances**
- Configured **NGINX** as the load balancer

### Google Cloud Platform (GCP)
- Deployed backend services on **Virtual Machines**
- Implemented a **dedicated VM** to run the load balancer with all six algorithms

---

## Testing & Evaluation

A combination of **load testing**, **security scanning**, and **cloud monitoring tools** was used to rigorously assess performance under varying traffic conditions, including stress and simulated DDoS attacks.

### Tools Used

#### Load Testing & Traffic Generation
- Apache JMeter
- Apache Benchmark
- Locust
- K6

#### Security Assessment
- NMap
- OWASP ZAP

#### Monitoring
- AWS CloudWatch
- GCP Monitoring

---

### Evaluated Metrics
- Response Times (Average, P95)
- Throughput (requests/sec)
- Traffic Distribution
- CPU & Memory Utilization
- Connection Stability & Blocking Time
- Request Failures / Error Rates
- Health Check Pass Rates
- ZAP-based Security Risk Scores

---

## Key Findings

### Performance
- **Random algorithm** had the **highest throughput**
- **Round Robin** had the **shortest average response time**
- **Least Connections** provided the **best balance** between speed and resource usage

### Availability
- **Round Robin** had **zero HTTP failures**, **zero downtime**, and **excellent health check scores**

### Scalability
- **Random** demonstrated **highest throughput** with **low connection overhead**
- **Round Robin** had **fastest P95 response time**, though with higher overhead

### Security
- All algorithms showed **low vulnerability** to DDoS, Slowloris, and SQL Injection
- **Round Robin** was the fastest under simulated security attacks

---

## Optimization Outcome

- Stress tests with **Python scripts** and **NMap** helped **identify performance bottlenecks**
- System performance improved by **40%** during peak load after tuning

---

## Conclusion

This project presents a robust, empirical framework to understand trade-offs across load balancing strategies in cloud environments. The insights here can guide architecture design and optimization decisions for highly available, scalable, and secure distributed systems.
