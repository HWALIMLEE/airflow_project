Airflow tutorial
---

Apache Airflow tutorial 코드입니다. 

## Contents

| Part | Title                                                                                                                                                               |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | [Introduction to Apache Airflow](https://amazelimi.tistory.com/entry/Airflow-1)                                                                                     |
| 2    | [Set up airflow environment with docker]()                                                                                                                          |
| 3    | [Set up airflow in local](https://amazelimi.tistory.com/entry/Airflow-local-%EC%84%A4%EC%B9%98)                                                                     |
| 4    | [Airflow Dag Creation Boilerplate Code](https://amazelimi.tistory.com/entry/Airflow-DAG-Boilerplate-CLI-%EB%8F%84%EA%B5%AC-%EC%83%9D%EC%84%B1-LIM)                  |
| 5    | [Build a Dag Pipeline Using Google Cloud Bigquery]() |


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

- Clone this repo
- Install the prerequisites
- Run the service
- Check http://localhost:8080
- Done! :tada:

### Prerequisites

- Install [Docker](https://www.docker.com/)
- Install [Docker Compose](https://docs.docker.com/compose/install/)
- Following the Airflow release from [Python Package Index](https://airflow.apache.org/docs/apache-airflow/2.4.3/installation/installing-from-pypi.html)

### Supportability

**Docker Service with `make` cli**

```
make init

# Build the image
# docker build . -t airflow:2.4.3
```

```
make start

# Docker compose up
# docker-compose -f docker-compose.yml up -d
```

```
make stop

# Docker compose down
# docker-compose down --volumes
```

Check http://localhost:8080/

```
User: airflow
Password: airflow
```

**DAG Creation BoilerPlate CLI**
```
make create

example
? dag name  movie_etl
? description  영화평점 데이터 etl 작업 dag
? owner  hwalim
? retries  3
? retry delay minutes  1
? start date (ex. 2023, 1, 1, 17, 30)  2023, 1, 1, 17, 30
? schedule interval  @daily
? catchup  False
? tags  etl
```# airflow_project
