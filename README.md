# WK13-Homework-And-Project

ELK Stack Deployment

All files used in this repository were applied to set up the network below

![alt text](https://github.com/GHanna25/WK13-Homework-And-Project/blob/main/DIAGRAMS/elk-diagram.png)

The scripts and files used to install these programs and architecture are listed below

[Filebeat-playbook.yml](https://github.com/GHanna25/WK13-Homework-And-Project/blob/main/ANSIBLE/Filebeat/filebeat.yml) 

[metricbeat-playbook.yml](https://github.com/GHanna25/WK13-Homework-And-Project/blob/main/ANSIBLE/Metric%20Beat/metricbeat.yml)

[elk-vm-playbook](https://github.com/GHanna25/WK13-Homework-And-Project/blob/main/ANSIBLE/ELK%20Stack/elkvm.yml)

[docker-playbook](https://github.com/GHanna25/WK13-Homework-And-Project/blob/main/ANSIBLE/Docker/pentestdocker.yml)


This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
- Beats in Use
- Machines Being Monitored
- How to Use the Ansible Build


**Description of the Topology**
The purpose of this network is to expose a monitored instance of DVWA. Enabling Load-Balancing ensures the applications will be secure while also protecting against potential threats and attacks to the network.This network features a jumpbox which is used for secured external network access. A jumpbox is also used for System Administrating so all admins that perform any tasks must connect to the jumpbox which creates a safer environment. Filebeat records data and log events and sends the information to elasticsearch. Metricbeat records data of the OS and other services that are running on these servers.


**Access Policies**
The machines on the internal network are not exposed to the public Internet.
The Jumpbox is the only machine that can accept connections from the internet.
The only IP that can connect through the jumpbox is my host machinees IP.
Machines that are within the network are only accessible via Docker.
The IP of the jumpbox is 20.213.123.120

**ELK Configuration**
Ansible was used to automate all configuration of the machines. No configuring was performed manually. By automating the configuration it simplified our tasks sand saved us time which allowed everything to be much easier than going in and performing these repetitive tasks manually.

The following screenshot shows the result of successfully connecting to the docker.
[!alt text](![container-connect](https://user-images.githubusercontent.com/97201701/167530310-398db1ed-ea76-4d86-a94b-d4a0ae0afb75.png)



I have installed the following programs on these machines.

- Filebeat and Metricbeat

- Filebeat is a lightweight shipper that centralizes log data. It also monitors log files, collects log events, and will forward them to Logstash or Elasticsearch.

- Metricbeat collects data metrics from the OS and other services that are running. It then takes the stats it collects and ships them to whichever output you specify.




