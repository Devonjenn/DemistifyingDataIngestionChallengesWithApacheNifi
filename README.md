# DemistifyingDataIngestionChallengesWithApacheNifi
Unlock insights into data challenges with 'Demystifying Data Ingestion Challenges.' Navigate obstacles with Apache NiFi, an open-source integration tool, simplifying data flow, and transforming how you handle diverse data formats and large volumes.


**INstall driver to postgres**

PostgreSQL Driver

docker exec -it nifi_container_persistent curl https://jdbc.postgresql.org/download/postgresql-42.2.23.jar --output /opt/nifi/nifi-current/lib/postgresql-42.2.23.jar

**SPECIFIC PROPERTIES FOR the DCBPCOnnectionPool**
jdbc:postgresql://postgres:5432/mydb

org.postgresql.Driver

file:///opt/nifi/nifi-current/lib/postgresql-42.2.23.jar

schema name
public



**Copy files to the docker container**

docker exec -it nifi_container_persistent /bin/bash
mkdir files
docker cp Titanic.parquet nifi_container_persistent:/opt/nifi/nifi-current/files
