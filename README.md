# Ansible AWS Jupyter Spark

Ansible Script to install Jupyter and Spark on a EC2 Instance

## Ansible

 ansible-playbook -i hosts -l servers -u ubuntu install.yml

## Spark

/opts/spark/sbin/start-master.sh -h <server_ip> <br />
/opts/spark/sbin/start-slave.sh -h <master_url> <br />

## Jupyter

jupyter notebook --config=/home/ubuntu/.jupyter/jupyter_notebook_config.py


```python
import findspark
findspark.init()
import pyspark
import random

sc = pyspark.SparkContext(appName="test", master="<master_url>")
```
