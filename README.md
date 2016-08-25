# monitoring-ansible

Collection of Ansible playbooks for deploying and evaluating monitoring tools on Ubuntu 14.04.

* [Elasticsearch](https://www.elastic.co/products/elasticsearch)
* [Kibana](https://www.elastic.co/products/kibana)
* [Logstash](https://www.elastic.co/products/logstash)
* [Sensu](https://sensuapp.org) (with [Uchiwa](https://www.uchiwa.io))
* [InfluxDB](https://influxdata.com/time-series-platform/influxdb/)
* [Telegraf](https://influxdata.com/time-series-platform/telegraf/)
* [Kapacitor](https://influxdata.com/time-series-platform/kapacitor/)
* [Chronograf](https://influxdata.com/time-series-platform/chronograf/)
* [Grafana](http://grafana.org/)

## Requirements

This repository is developed with the following dependencies.

* Vagrant 1.8.1 + VirtualBox 5.0.14
* Ansible 2.0.2.0

## Usage

Start by cloning the repository from GitHub.

```bash
git clone https://github.com/ianunruh/monitoring-ansible.git
cd monitoring-ansible
```

Then bring up one of the Vagrant scenarios (currently just `minimal`)

```bash
cd vagrant/minimal
vagrant up
```

This will automatically apply the `vagrant/minimal/kitchen-sink.yml` playbook against the VMs.
Afterwards, you will be able to access the various monitoring tools through their respective
interfaces on the `analytics1` host via `10.10.0.100`.
