---
description: The sauce behind the Ricochet Keeper!
---

# 💨 - Apache Airflow

## What is Apache Airflow?

Airflow is a platform to programmatically author, schedule, and monitor workflows.

Airflow is used to author workflows as Directed Acyclic Graphs (DAGs) of tasks. The Airflow scheduler executes your tasks on an array of workers while following the specified dependencies. Airflow's rich command line utilities make performing complex surgeries on DAGs a snap. The easy-to-use web interface makes it easy to visualize pipelines running in production, monitor progress, and troubleshoot issues when needed. [\[1\]](https://airflow.apache.org/docs/apache-airflow/stable/index.html)

![Ricochet keeper workflow for call \`distribute\` method on all exchange contracts ](<../.gitbook/assets/Screen Shot 2021-09-18 at 11.56.08 AM.png>)

## How does Ricochet Exchange use Apache Airflow?

Ricochet exchange uses Apache Airflow as a "keeper" to perform tasks automatically based on a schedule. Task performed by the Airflow-based keeper include:

* Submitting `distribute` transactions to each exchange contract
* Monitoring streamers balances and calling `closeStream` when balances run low
* Acting as a price reporter and calling `submitValue` on Tellor's contracts

![](<../.gitbook/assets/Screen Shot 2021-09-18 at 12.03.16 PM.png>)
