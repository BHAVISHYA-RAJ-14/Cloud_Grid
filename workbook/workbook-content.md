*## 1. Case Study Definition*



*### Case Study Name*

*Cloud\_Grid*



*### Description*

*It is a cloud-native monitoring and security architecture designed to track website availability and detect cloud misconfigurations using CIS-aligned policies.*



*The system focuses on reliability, observability, and proactive security while maintaining read-only access to cloud environments.*



*### Core Features*

*- Website uptime and latency monitoring*

*- Automated health check scheduling*

*- Cloud configuration security scanning*

*- CIS benchmark alignment*

*- Risk scoring and compliance reporting*



*### User Roles*

*- Developer*

*- Cloud Administrator*

*- Security Engineer*

*- Startup Founder*



*## 2. User Personas*



*### Persona 1 – Developer*

*A backend developer responsible for maintaining application uptime and performance.*



*### Persona 2 – Security Engineer*

*Responsible for identifying and mitigating cloud misconfigurations without impacting production.*



*## User Stories*

*- As a developer, I want to monitor uptime so failures are detected early.*

*- As a security engineer, I want to detect misconfigurations before exploitation.*

*- As an admin, I want compliance-aligned reports for audits.*



*## 3. SLIs and SLOs*



*| Capability | SLO | SLI |*

*|-----------|-----|-----|*

*| Website Monitoring | 99.9% availability | Successful HTTP checks |*

*| Monitoring API | 95% < 300ms | API latency |*

*| Security Scanning | 100% coverage | Resources scanned |*

*| Alerting | < 2 minutes | Detection-to-alert time |*





\## 4. Microservices Design



\### Services

\- Web UI Service

\- Monitoring API Service

\- Health Check Worker

\- Cloud Configuration Collector

\- Normalization Engine

\- CIS Rules Engine

\- Reporting \& Analytics Service



All services are stateless and communicate via asynchronous messaging.





\## 5. REST API Design



| Service | Endpoint | Method |

|------|---------|--------|

| Monitoring API | /urls | POST |

| Monitoring API | /results | GET |

| Security Scanner | /scan | POST |

| Security Scanner | /findings | GET |





\## 6. Storage Design



| Service | Data Type | Storage | Consistency |

|-------|----------|--------|------------|

| Monitoring | Structured | NoSQL | Eventual |

| Security Scanner | Semi-structured | NoSQL | Eventual |

| Reports | Structured | Object Storage | Strong |





\## 7. Networking

\- HTTPS-only access

\- Internet-facing UI

\- Internal service communication



\## 8. Reliability

\- Stateless services

\- Horizontal scaling

\- Retry-based fault tolerance



\## 9. Disaster Recovery

\- Immutable rule sets

\- Configuration re-scanning

\- Multi-region design assumption



\## 10. Security

\- Least-privilege IAM

\- Read-only cloud access

\- Audit logging



\## 11. Cost Estimation

Designed to operate within free-tier limits using serverless services.

