# Task 3 Write-up: Git-backed Job Scheduling

## Databricks Job Run URL

Paste the URL of your successful Job run from the Databricks UI address bar:
https://adb-7405619530719547.7.azuredatabricks.net/jobs/402767432860412/runs/733351880002668?o=7405619530719547
`___`

## Screenshots

Ensure the following screenshot files exist in `task-3/screenshots/`:

1. `job_config.png` — Showing the dbt task configuration with Git repository URL, branch `main`, path `task-2`, and warehouse `hyf-dbt-warehouse`.
2. `job_run_success.png` — Showing a successful run log with a green checkmark and stdout execution output.
3. `job_schedule_paused.png` — Showing the scheduled trigger set to **Paused**.

## Orchestration Comparison

### When would you choose Databricks Jobs versus Apache Airflow for pipeline orchestration?

Write two to three sentences comparing Databricks Jobs and Apache Airflow in your own words:

Databricks Jobs is a good choice when the pipeline runs mainly inside the Databricks platform, for example running dbt models, notebooks, or Spark jobs. It provides simple scheduling and monitoring without extra infrastructure. Apache Airflow is better when orchestrating complex workflows across multiple systems, such as APIs, databases, cloud services, and different data platforms.