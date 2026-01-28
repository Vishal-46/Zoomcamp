# Zoomcamp Notes

## Module 1 – Data Ingestion
- Outline ETL pipeline setup
```bash
python ingest.py --source taxi --target postgres
```

## Module 2 – Workflow Orchestration
- Prefect flows and scheduling basics
```python
with Flow("ingestion") as flow:
    run_extract() >> run_load()
```

## Module 3 – Data Warehouse
- BigQuery tables and partitioning notes
```sql
CREATE TABLE trips PARTITION BY DATE(pickup_datetime);
```

## Module 4 – Analytics Engineering
- dbt models and testing checklist
```yaml
tests:
  - unique
  - not_null
```

## Module 5 – Batch Processing
- Spark jobs and optimization reminders
```python
df.repartition("pickup_zone").write.parquet(path)
```

## Module 6 – Streaming
- Kafka topics and consumer hints
```bash
kafka-console-consumer --topic trips --from-beginning
```

## Capstone Project
- To-do list and milestones status
```markdown
- [x] Define scope
- [ ] Deploy MVP
```