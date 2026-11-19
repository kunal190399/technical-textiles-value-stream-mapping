# Value Stream Mapping & Process Optimisation for Technical Textiles

**Planned build · SQL, Python and value-stream maps**

**Decision.** A production supervisor needs to choose between changing batch release and reducing changeover time. The longest processing step may differ from the queue that causes the longest delay.

| Milestone | Work | Acceptance check |
|---|---|---|
| 1. Map the current state | Trace one family from order release through weaving, coating and fabrication to finished-goods receipt. Map planning signals, queues, rework loops and batch handoffs. | Every elapsed interval has a defined start, end and classification. The map reconciles to one worked batch timeline. |
| 2. Establish a baseline | Generate timestamped events per batch and operation. Use SQL to calculate queue, setup and processing times. Use Python to summarise median and 90th-percentile end-to-end lead time, throughput, yield and work in progress. | Check event ordering, rework and unfinished batches. State the observation window and how incomplete orders are counted. |
| 3. Compare changes | Simulate a capped release queue and a shorter coating changeover, separately and together. Hold incoming orders, shift capacity and initial stock constant. Repeat paired runs across seeds. | Report relative median lead-time reduction against baseline, variation across runs and any throughput or quality penalty. Test the 20% reduction target. |
| 4. Plan adoption | Draft a one-shift pilot. Operators record exceptions, the supervisor reviews queue and quality measures, and the planner adjusts release rules. Include training, feedback and a rollback rule. | Publish both maps, reproducible analysis, a scenario comparison and a stakeholder plan naming the decision owner and review cadence. |

**First session.** Draw the route of a single batch. Create one event log with a wait before coating and one rework loop. Verify release-to-receipt time by hand before scaling the simulation.
