# Optional exploratory data analysis
Open `data/northstar.sqlite` in any SQLite client or use Python sqlite3/pandas. Start with row counts, missingness, duplicate IDs and join cardinalities. Use UTC and the June 30 cutoff; exclude unresolved tickets from completed-resolution averages and report their number. Response SLA is measured against policy hours; tickets without response may already have breached at cutoff. Do not confuse response SLA with resolution SLA.

```sql
SELECT substr(created_at,1,7) AS month, count(*) AS tickets FROM tickets GROUP BY 1 ORDER BY 1;
SELECT historical_department, assigned_department_id, count(*) AS n FROM tickets GROUP BY 1,2;
SELECT t.product_id, count(*) AS tickets, count(DISTINCT t.incident_id) AS incidents FROM tickets t GROUP BY 1;
SELECT strftime('%w',created_at) AS weekday, avg((julianday(first_response_at)-julianday(created_at))*24) AS response_hours FROM tickets WHERE first_response_at IS NOT NULL GROUP BY 1;
SELECT s.tier, count(*) AS responded, avg(CASE WHEN (julianday(t.first_response_at)-julianday(t.created_at))*24>s.first_response_hours THEN 1.0 ELSE 0.0 END) AS breach_share_responded FROM tickets t JOIN sla_policies s USING(sla_policy_id) WHERE first_response_at IS NOT NULL GROUP BY 1;
```
Investigate volume spikes, incident links, payment failures, transfers, weekend delays and feedback selection bias. Compare cohorts with denominators; avoid claiming causation from correlations. Submit notebook or SQL, charts, data-quality report, 3 evidence-backed insights and recommendations. Optional scoring: preparation 15, approach 20, manipulation 20, visualization 15, insight 20, communication 10. Separate from FDE score.
