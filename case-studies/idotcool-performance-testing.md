# iDotCool — Website Performance Testing with Apache JMeter

## 1. Project Overview

**Application:** [idotcool.com](https://idotcool.com/)  
**Testing Type:** Performance Testing  
**Tool:** Apache JMeter 5.x  
**Role:** Software Quality Assurance Engineer

This project involved evaluating the performance and reliability of the iDotCool website under increasing simulated user loads. The testing focused on response times, request failures, throughput, and received bandwidth across nine website pages.

## 2. Testing Objectives

- Evaluate website performance under different concurrent user loads.
- Identify performance degradation and potential capacity limits.
- Measure average response time, estimated 90th-percentile response time, error rate, throughput, and received bandwidth.
- Identify pages requiring further performance investigation.

## 3. Test Scope

The following pages were included:

- Home Page
- About Us
- Services
- Portfolio
- Esthetic Fest
- Gandhara-Fest
- Blog
- Blog Category
- Contact

### Test Scenarios

- **Load testing:** 5, 10, and 15 simulated users.
- **Stress testing:** Increased load up to 20 users.
- **Traffic-surge assessment:** Evaluated performance behavior at higher loads. A dedicated spike-test configuration was not documented separately.

The documented test configuration used a 30-second ramp-up and one loop iteration per scenario unless otherwise specified.

## 4. Key Results

| Metric | 5 Users | 10 Users |
|---|---:|---:|
| Average response time | 3,522 ms | 10,214 ms |
| Estimated 90th percentile | 5,017 ms | 21,359 ms |
| Error rate | 2.50% | 26.25% |
| Throughput | 0.59 req/sec | 0.67 req/sec |
| Received bandwidth | 15.84 KB/sec | 14.21 KB/sec |

At 20 users, the report recorded a 100% request failure rate. Detailed numerical results for the 15-user scenario were unavailable.

## 5. Key Findings

### Performance degradation under increased load

The overall average response time increased from approximately 3.5 seconds at 5 users to 10.2 seconds at 10 users. The error rate also increased substantially, while throughput improved only marginally.

### Pages requiring investigation

- **Portfolio:** A reported 20% error rate at 5 users.
- **Home Page:** A reported 50% error rate at 10 users.
- **About Us:** A reported 60% error rate at 10 users.

These findings identified areas requiring further investigation; the tests alone did not establish the underlying causes.

### Capacity and reliability concerns

The reported 100% failure rate at 20 users indicated that the tested configuration could not successfully process requests at that load during the test run. Server capacity limitations and traffic filtering were possible explanations, but neither was confirmed through server-side monitoring.

## 6. QA Responsibilities and Approach

- Configured and executed performance test scenarios using Apache JMeter.
- Simulated increasing user loads against selected website pages.
- Collected and analyzed response-time, error-rate, throughput, and bandwidth metrics.
- Compared results across load levels to identify performance degradation.
- Identified pages with elevated failure rates for further investigation.
- Documented findings and recommendations for follow-up testing.

## 7. Recommendations

- Investigate the errors observed on the Portfolio, Home Page, and About Us pages.
- Review server logs and infrastructure metrics to identify the causes of failed requests.
- Check resource utilization, connection handling, and request timeouts.
- Verify whether traffic filtering or Cloudflare protection affected the test results.
- Repeat tests at intermediate loads and perform additional runs to validate consistency.
- Conduct further testing after any performance improvements.

## 8. Conclusion

The recorded test results showed substantial performance degradation between 5 and 10 simulated users, with a reported 100% request failure rate at 20 users. The findings highlighted the need for further investigation into response times, failed requests, and capacity limitations.

This case study demonstrates practical experience with Apache JMeter, performance test execution, metrics analysis, and reporting evidence-based findings.

**Note:** Results represent the documented test run and do not establish the website's current performance or confirmed infrastructure root causes. The 90th-percentile values were estimates calculated from average response time and standard deviation.
