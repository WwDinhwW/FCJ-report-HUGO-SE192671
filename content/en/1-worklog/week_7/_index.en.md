---
title: "Week 7: Backend System Optimization and Expanding AWS Cost Monitoring Features"
type: "page"
weight: "7"
---

# Objectives:
* Develop and extend key backend API routes (CloudWatch, Cost Explorer, S3, SecurityHub).
* Optimize asynchronous processing and enhance caching performance with Redis.
* Deepen understanding of Python’s runtime behavior, the GIL (Global Interpreter Lock), and parallel processing.
* Strengthen cost visibility and performance analysis through custom AWS monitoring APIs.

# Tasks Completed:
| Day | Tasks                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Sources                   |
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------|-------------------------------------|
| Mon | - Worked at the office to add **api/routes/cloudwatch.py** for monitoring data collection. <br> - Optimized log-handling functions and implemented caching for CloudWatch data using Redis.                                                      | 20/10/2025 | 20/10/2025      | AWS Docs, mentor guidance, Internet |
| Tue | - Added **api/routes/costexplorer.py** to aggregate and analyze AWS service costs. <br> - Enhanced concurrent query execution and caching to reduce API response latency.                                                                        | 21/10/2025 | 21/10/2025      | AWS Docs, Internet, mentor guidance |
| Wed | - Implemented **api/routes/s3.py** for S3 data access. <br> - Studied IAM Policy control and cost optimization methods in S3 through data tiering (Storage Classes).                                                                             | 22/10/2025 | 22/10/2025      | AWS Docs, Internet, mentor guidance |
| Thu | - Updated the **Report Site** content, adding a new “Cloud Optimization” section to document cost management practices. <br> - Authored internal guide on configuring caching and async tasks in the project.                                    | 23/10/2025 | 23/10/2025      | Internet, mentor-provided materials |
| Fri | - Added **api/routes/securityhub.py** for security alert aggregation. <br> - Researched Python’s internal behavior: GIL, async, and parallel execution. <br> - Improved Redis/FastAPI workflow integration and efficiency in backend operations. | 24/10/2025 | 24/10/2025      | Internet, internal documentation    |

# Results:
* Completed development of key backend API routes: CloudWatch, Cost Explorer, S3, and SecurityHub.
* Significantly improved backend performance through caching and asynchronous processing.
* Gained deeper insight into Python’s internal mechanisms and optimized FastAPI’s concurrency handling.
* Initiated **Cloud Optimization** implementation in the project — focusing on cost monitoring and performance tuning.
* Strengthened backend engineering, resource management, and system efficiency skills.