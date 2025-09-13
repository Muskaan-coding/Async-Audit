### 🔧 Details
- Enabled async support in `MainApplication`
- Added custom thread pool via `AsyncConfig`
- Refactored `UserService` methods to use `CompletableFuture`
- Offloaded audit logging using `runAsync`
- Updated controller methods to return async responses

### 📈 Results (JMeter)
| Metric        | Sync        | Async       |
|---------------|-------------|-------------|
| Avg Time      | 220 ms      | 15 ms       |
| Max Time      | 255 ms      | 297 ms      |
| Throughput    | 48 req/sec  | 114 req/sec |
| Error Rate    | 0%          | 0%          |

Tested with 100 unique users using JMeter and identical test plan.

✅ Improves response time and system scalability.

📄 [View full SyncReport.html](https://html-preview.github.io/?url=https://github.com/Muskaan-coding/Async-Audit/blob/master/performance_Dashboards_Jmeter/sync-report/index.html)  

📄 [View full AsyncReport.html](https://html-preview.github.io/?url=https://github.com/Muskaan-coding/Async-Audit/blob/master/performance_Dashboards_Jmeter/async-report/index.html)
