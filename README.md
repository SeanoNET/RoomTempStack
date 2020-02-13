# RoomTempStack

Production swarm stack repo for monitoring temperature and humidity data

## Services

- [RoomTempDevice-MQTT](https://github.com/SeanoNET/RoomTempDevice-MQTT) ![Build Docker CLI](https://github.com/SeanoNET/RoomTempMQTTConsumer/workflows/Build%20Docker%20CLI/badge.svg) sends sensor data from a MXChip AZ3166 IoT Devkit to a MQTT Broker.
- [eclipse-mosquitto](https://hub.docker.com/_/eclipse-mosquitto) Eclipse Mosquitto is an open source message broker which implements MQTT version 5, 3.1.1 and 3.1.
- [postgres](https://hub.docker.com/_/postgres) The PostgreSQL object-relational database system provides reliability and data integrity.
- [RoomTempDashboard](https://github.com/SeanoNET/RoomTempDashboard/) ![Build Docker CLI](https://github.com/SeanoNET/RoomTempDashboard/workflows/Build%20Docker%20CLI/badge.svg) Web dashboard for displaying temperature and humidity data.
- [Grafana](https://hub.docker.com/r/grafana/grafana/) Grafana is the open source analytics and monitoring solution for every database.

## Install

Clone this [repository](https://github.com/SeanoNET/RoomTempStack)

`git clone https://github.com/SeanoNET/RoomTempStack.git`

Init swarm with `docker swarm init` and deploy stack `docker stack deploy --compose-file docker-compose.yml roomtempstack`

If running on an arm32 device like the Raspberry Pi run:

Init swarm with `docker swarm init` and deploy stack `docker stack deploy --compose-file docker-compose-linux-arm.yml roomtempstack`