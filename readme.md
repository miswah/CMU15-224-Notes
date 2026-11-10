This repo is for [CMU15-224](https://15445.courses.cs.cmu.edu/fall2025/) course from [Youtube](https://youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5&si=H9ZcBiAEg9WzNYS4) the course is taught in C++ so the supplimenty labs are from [6.5830/6.5831: Database Systems](https://dsg.csail.mit.edu/6.5830/) (Github Repository)[https://github.com/MIT-DB-Class/simple-db-hw-2022.git] [Youtube](https://www.youtube.com/playlist?list=PLfciLKR3SgqOxCy1TIXXyfTqKzX2enDjK)




# Database Systems Roadmap: CMU 15-445 + MIT SimpleDB

| Phase | CMU 15-445 Lectures (Watch) | MIT SimpleDB Lab (Code in Java) | Key Implementation Focus & Milestone |
| --- | --- | --- | --- |
| **Phase 1: Storage & Buffer Pool** | 01\. Relational Model\<br\>02\. Modern SQL\<br\>03\. Database Storage I\<br\>04\. Database Storage II\<br\>05\. Buffer Pools | **Lab 1: Storage Management** | \- Tuple, TupleDesc, and field layout.\<br\>\- Binary serialization: `HeapPage` and `HeapFile`.\<br\>\- Page caching & eviction: `BufferPool`.\<br\>\- **Milestone:** Pass `ant test -Dtest=HeapFileReadTest`. |
| **Phase 2: Access Methods & Operators** | 06\. Hash Tables\<br\>07\. Tree Indexes (B+ Trees)\<br\>08\. Index Concurrency\<br\>09\. Sorting & Aggregations\<br\>10\. Join Algorithms\<br\>11\. Query Execution I | **Lab 2: SimpleDB Operators** | \- Volcano iterator interface: `DbIterator`.\<br\>\- Operators: `Filter`, `Join` (nested loops / hash), and `Aggregate`.\<br\>\- Modifying state: `insertTuple` and `deleteTuple` on disk pages.\<br\>\- **Milestone:** Execute full SQL queries via the SimpleDB CLI parser. |
| **Midterm Checkpoint** | Review Break | Consolidation | \- Work through the MIT Midterm Exam.\<br\>\- Review Storage, B+ Trees, and Join I/O calculations to verify theoretical understanding. |
| **Phase 3: Transactions & Concurrency** | 15\. Concurrency Control Theory\<br\>16\. Two-Phase Locking (2PL)\<br\>17\. Timestamp Ordering\<br\>18\. Multi-Version Concurrency (MVCC) | **Lab 3: Transactions & Locking** | \- Page-level Strict Two-Phase Locking (Strict 2PL).\<br\>\- Shared vs. Exclusive locks using `java.util.concurrent`.\<br\>\- Deadlock detection via Wait-For Graph cycle detection.\<br\>\- **Milestone:** Pass `ant runtest -Dtest=TransactionTest`. |
| **Phase 4: Query Optimization** | 12\. Query Execution II\<br\>13\. Query Optimization I\<br\>14\. Query Optimization II | **Lab 4: Selinger Optimizer** | \- Single-table cardinality estimation with histograms.\<br\>\- Join size and cost estimation.\<br\>\- Optimal join order using dynamic programming (`O(2^N)` space).\<br\>\- **Milestone:** Pass `ant runtest -Dtest=QueryPlanTest`. |
| **Phase 5: Logging & Recovery** | 19\. Logging Protocols\<br\>20\. Crash Recovery (ARIES)\<br\>21\. Distributed Databases (Optional) | **Lab 5: Rollback & Recovery** | \- Write-Ahead Logging (WAL) format.\<br\>\- Transaction abort / rollback using undo logs.\<br\>\- Crash recovery: redo committed, undo uncommitted.\<br\>\- **Milestone:** Pass `ant systemtest -Dtest=AbortEvictionTest`. |
| **Final Checkpoint** | Wrap-up | Review | \- Review MIT Final Exam questions.\<br\>\- Strict 2PL anomalies.\<br\>\- ARIES analysis, redo, and undo passes.\<br\>\- View serializability. |

---
