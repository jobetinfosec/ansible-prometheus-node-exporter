# Install Prometheus Node Exporter module using Ansible


## Description

Install Prometheus Node Exporter module using Ansible configuration management tool.



## Requisites

a) Cloud Platform account<br />
b) A VPS server (any Linux distro) with your public SSH key already installed<br />



## Instructions

a) On your laptop create a working directory


b) In your working directory open a console window


c) Clone github repository

```
git clone https://github.com/jobetinfosec/ansible-prometheus-node-exporter.git
```


d) Switch to ansible-prometheus-node-exporter directory

```
cd ansible-prometheus-node-exporter
```


e) Check if you able to ping remote server

```
ansible -m ping all
```

You should receive a SUCCESS message


f) Open your browser and then open the Node Exporter releases page, and take note of the latest release's number

```
https://github.com/prometheus/node_exporter/releases
```


g) Open roles/node_exporter/defaults/main.yml file

```
nano roles/node_exporter/defaults/main.yml
```


h) Change the <LATEST_RELEASE> item with the number of the latest Node Exporter release, then save the file



i) Check if any error shows up

```
ansible-playbook node.yml --check
```


j) Launch installation

```
ansible-playbook node.yml
```
