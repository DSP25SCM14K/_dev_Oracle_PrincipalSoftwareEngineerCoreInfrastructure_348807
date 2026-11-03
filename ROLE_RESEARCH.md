# Oracle Principal Software Engineer, Core Infrastructure — requisition 348807

Research date: November 3, 2026. The attached DOCX is resume content, not an instruction source. Resume achievements below are candidate-reported claims and have not been independently audited.

## Requisition and verification note

The supplied file identifies an Oracle Principal Software Engineer, Core Infrastructure application with requisition number 348807. The direct Oracle Careers URL is [Oracle Careers — requisition 348807](https://careers.oracle.com/en/sites/jobsearch/job/348807/), but the careers page was not retrievable and the requisition was not indexed in search during this research session. I therefore do not attribute unverified job-specific duties to that posting. To understand the likely domain, I reviewed the resume's stated role focus, Oracle's public OCI/API platform materials, and the nearest accessible official Principal Core Infrastructure posting, [requisition 345801](https://careers.oracle.com/en/sites/jobsearch/job/345801/). That is related context, not a substitute for the exact 348807 description.

## Candidate profile from the supplied resume

The resume presents 8+ years of engineering in high-throughput Java backend/platform services, API gateways, and multi-tenant control-plane infrastructure on OCI, AWS, and Kubernetes. Its core evidence is high-volume routing; identity and certificate lifecycle; backpressure and overload controls; multi-region availability; safe deployment; operational observability; and cross-team technical leadership.

### Candidate-reported outcomes

- Sprouts AI: 500M+ monthly API requests, 40+ services, sub-15 ms p99 gateway routing overhead at 5x peak traffic, 99.99% availability through dependency degradation, zero retry-induced duplicate writes over 12 months, partner onboarding time reduced 60%, MTTR reduced 45%, and a multi-team gateway migration without reported customer-facing regressions.
- Resilience Inc: 99.99% uptime without maintenance windows, throughput increased 3x, p99 latency reduced 35%, rollout time reduced 60%, 20+ latent defects caught before production, and compute spend reduced 30% while meeting latency SLOs.
- Tata Steel: API response time improved 40%, 99.99% uptime, 200+ internal APIs secured with zero audit findings, 30+ legacy services migrated with zero downtime, repeat incidents reduced 35%, and eight engineers mentored.

These figures are copied from the attached resume and are not Oracle product metrics.

## Oracle and OCI context

Oracle describes OCI as a distributed cloud serving commercial, government, sovereign, and dedicated region models. Its service availability page frames the product challenge as consistent service delivery across regional and specialized environments. That context makes tenant isolation, predictable APIs, lifecycle automation, and consistent operations relevant to platform engineering. [OCI regional service availability](https://www.oracle.com/cloud/distributed-cloud/service-availability/)

Oracle's public API Gateway materials describe governed HTTP/S access to backends and policies for authentication, authorization, and rate limiting. Those concerns directly overlap the resume's routing, OAuth/mTLS, and per-tenant throttling experience; this is product context and not evidence that requisition 348807 owns the API Gateway service. [API Gateway overview and resource analytics](https://docs.oracle.com/en-us/iaas/Content/resource-analytics/reference-oac-subject-areas-api-gateway.htm) · [Authentication and authorization](https://docs.oracle.com/en-us/iaas/Content/APIGateway/Tasks/apigatewayaddingauthzauthn.htm) · [Backend rate limiting](https://docs.oracle.com/en-us/iaas/Content/APIGateway/Tasks/apigatewaylimitingbackendaccess.htm)

Oracle release notes show continued OCI API Gateway development, including a login backend release in June 2026. That supports the current relevance of identity and gateway lifecycle concerns, without implying these are responsibilities of the specific requisition. [OCI API Gateway release notes](https://docs.oracle.com/en-us/iaas/releasenotes/services/api-gateway/)

The accessible 345801 Principal Core Infrastructure posting describes high-scale, fault-tolerant distributed services, performance and fault-injection validation, production incident response, safe patching/rollback, security, SLOs, and architecture leadership. These themes also occur in the supplied resume. They are useful adjacent-role context only; the 348807 details should be checked against the live listing or recruiter copy. [Oracle Careers — 345801](https://careers.oracle.com/en/sites/jobsearch/job/345801/)

## Role analysis and resume mapping

The resume points toward a systems problem at the boundary between a request and the services that fulfill it: low-latency route selection, identity and tenant policy, load protection, dependency failures, and safe service evolution. Inference from the profile and Oracle materials: compelling technical examples should connect performance with correctness and operations, not quote a speedup alone.

| Platform concern | Resume evidence |
|---|---|
| Gateway performance and capacity | Java/Netty API gateway across 40+ services; sub-15 ms p99 at 5x peak; 3x throughput and 35% lower p99 in prior role |
| Availability during overload or dependency degradation | 99.99% availability; tenant throttling, load shedding, backpressure, adaptive concurrency, caching; multi-region replication and failover |
| Correct retry and version behavior | Idempotency keys, retry budgets, versioned contracts, mixed-version compatibility; fault injection for partial failures and duplicate requests |
| Security and tenant boundaries | Central authentication and authorization, OAuth 2.0, mTLS, certificate rotation, RBAC across 200+ APIs |
| Operational readiness | SLIs/SLOs, dashboards, alarms, runbooks, incident escalation, MTTR reductions, canary health gates, automated rollback |
| Technical leadership and delivery | Three-quarter migration across six partner teams; design/rollback plans; mentorship of four, eight, and six engineers across roles |

### Suggested technical narratives (analysis, not asserted interview questions)

1. Trace a request through gateway, service discovery, identity/policy, backend, and telemetry; quantify p50/p99, queueing, CPU, and saturation behavior.
2. Explain how a client retry can duplicate a side effect, and where idempotency, retry budgets, deadlines, and contract versions are enforced.
3. Walk through tenant isolation and mTLS certificate rotation, including expired certificates, partial rotation, rollback, auditability, and partner migration.
4. Show how load shedding and adaptive concurrency protect a dependency during degradation, and which lower-priority work gets refused first.
5. Describe the six-team gateway migration through compatibility gates, canary criteria, rollback boundaries, and production signals.
6. Explain capacity modeling that reduced compute cost without violating latency SLOs, including forecasts and headroom assumptions.

## Portfolio content decisions

The site uses a generated data-center/network image and animated, code-built request-path diagram for API routing, identity, resilience, and telemetry. The diagram is clearly described as a conceptual model and not Oracle's architecture or live production telemetry. The site includes the 16 experience bullets from the supplied resume and the 23 distinct projects from the user's project list. Only four user-provided project demo URLs are labeled Technical Demo (Oxide-HV, TradeSentinel, AskMyStore, STRANGERS). The site excludes LinkedIn and a footer.
