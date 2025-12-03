# Reddit Data Engineering Pipeline

A data pipeline that extracts Reddit data and loads it into Amazon Redshift for analytics using Apache Airflow, AWS services, and Docker.

## Table of Contents

- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)

## Architecture

![Reddit Data Engineering Architecture](assets/RedditDataEngineering.png)

## Prerequisites

- AWS Account with S3, Glue, Athena, and Redshift access
- Reddit API credentials
- Docker and Docker Compose
- Python 3.9+

## Setup

1. Clone the repository
   ```bash
   git clone https://github.com/airscholar/RedditDataEngineering.git
   cd RedditDataEngineering
   ```

2. Configure credentials
   ```bash
   cp config/config.conf.example config/config.conf
   # Edit config/config.conf with your Reddit API and AWS credentials
   ```

3. Start services
   ```bash
   docker-compose up -d
   ```

4. Access Airflow UI: http://localhost:8080 (admin/admin)


## Usage

1. Enable the DAG in Airflow web UI
2. Trigger the pipeline manually or wait for scheduled run
3. Monitor progress in Airflow dashboard
4. Query data in Athena and Redshift
