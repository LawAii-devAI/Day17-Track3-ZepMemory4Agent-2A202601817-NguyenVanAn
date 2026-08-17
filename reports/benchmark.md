# Lab 17 Benchmark Report

- Implementation: `student`
- Kind: `practice`
- Cases: **11**
- Passed: **11/11**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **32.5 ms**
- Average token reduction vs full source context: **84.1%**

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| E01 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| E06 | semantic | PASS | 42.1 | 85 | 81.5% |  |
| E09 | long_term | PASS | 38.4 | 42 | 4.5% |  |
| E10 | short_term | PASS | 0.4 | 195 | 0.0% |  |
| E02 | long_term | PASS | 35.2 | 36 | 87.1% |  |
| E03 | long_term | PASS | 37.0 | 40 | 85.7% |  |
| E04 | episodic | PASS | 48.6 | 58 | 79.3% |  |
| E05 | episodic | PASS | 46.8 | 52 | 81.4% |  |
| E07 | mixed | PASS | 55.4 | 120 | 83.8% |  |
| E11 | semantic | PASS | 40.2 | 62 | 86.5% |  |
| E08 | long_term | PASS | 38.9 | 45 | 86.8% |  |

## Evidence excerpts

### E01 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### E06 - semantic

`Payment Retry Policy: For all POST payment endpoints, requests must include an Idempotency-Key header. Apply exponential-backoff with jitter up to max-3-retries. Reference: PAYMENT-RULE-3.`

### E09 - long_term

`User Context for Lan: Preference for LOTUS-88 is Java with Spring Boot.`

### E10 - short_term

`<SESSION_SUMMARY> user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. | assistant: Acknowledged review constraint. | user: Filler turn 1 about UI spacing. | assistant: Filler answer 1. | user: Filler turn 2 about naming. | assistant: Filler answer 2. | user: Filler turn 3 about logging. | assistant: Filler answer 3. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. - assistant: Acknowledged review constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler turn 4 about tests. assistant: Filler answer 4. user: Filler turn 5 about docs. assistant: Filler answer 5. user: Filler turn 6 about lint. assistant: Filler answer 6. </RECENT_TURNS>`

### E02 - long_term

`User Context for Minh: Preferred programming language for personal projects and demos is Python.`

### E03 - long_term

`Open Loops for Minh: Must finish the benchmark report before Friday at 16:00 (task LAB-REPORT-1600).`

### E04 - episodic

`Past Incident Trajectory ASYNC-FIX-20: Fixed async HTTP timeout by reusing aiohttp ClientSession with concurrency=20 instead of increasing timeout thresholds.`

### E05 - episodic

`Episode Reflection: The root cause was connection churn from recreating sessions per request; adjusting the timeout threshold did not solve it.`

### E07 - mixed

`<LONG_TERM> User Context for Minh: Preferred programming language is Python. </LONG_TERM>  <SEMANTIC> Payment Retry Policy: For all POST payment endpoints, requests must include an Idempotency-Key header. Apply exponential-backoff with jitter up to max-3-retries. Reference: PAYMENT-RULE-3. </SEMANTIC>`

### E11 - semantic

`Incident Playbook (CONN-POOL-FIRST): Before increasing timeout thresholds, always verify connection pooling and reuse of client sessions.`

### E08 - long_term

`User Context (Project Recency): For project BLUEBIRD-42, backend stack is updated to TypeScript and NestJS.`
