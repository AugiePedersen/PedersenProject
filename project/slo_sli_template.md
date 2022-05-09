# API Service

| Category     | SLI                                                      | SLO                                                                                                         |
|--------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Availability | Percentage of successful requests over last 5 minutes    | 99%                                                                                                         |
| Latency      | 90% of requests finish in 100ms                          | 90% of requests below 100ms                                                                                 |
| Error Budget | Successful requests / all request must be < 80%          | Error budget is defined at 20%. This means that 20% of the requests can fail and still be within the budget |
| Throughput   | Successful Requests per second                           | 5 RPS indicates the application is functioning                                                              |
