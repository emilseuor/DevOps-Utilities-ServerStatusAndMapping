# Getting Started

This creates a historic list of ups and downs in servers status with geoposition for mapping. It gets the list of servers from Zabbix API 4.0,
the geohash can be obtained from latitude, longitude data. It can be stored in any DB. In this case it comes with a connection to Influx but
can be modified to MongoDB, SQL Server or any other.

## Installation

Make a copy of this project and point it to the new environment.

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the dependencies.

```bash
pip install json
pip install requests
pip install influxdb
```

## Usage

get_hostgroups.py Gets a list of Available Hostgroups in Zabbix
get_servers_status.py Gets a list of servers with their location data and current status (up / down), filtered by the chosen Hostgroups and this data is saved in a db with datetime.

```python
# Configuration - Zabbix Data
ip_or_address = '000.000.000.000'
usr = 'MY ZABBIX USER'
psw = 'MY ZABBIX API KEY'
```


```python
# Configuration - Zabbix Data
zabbix_host = '000.000.000.000'
url = 'http://' + zabbix_host + '/zabbix/api_jsonrpc.php'
usr = 'ZABBIX USER'
psw = 'ZABBIX API KEY'

#INFLUXDB CONNECTION DETAILS
host = '000.000.000.000'
port = '8080'
user = 'INFLUX USER'
password = 'INFLUX PASSWORD!'
dbname = 'DB NAME'
dbuser = 'DB USER'
dbuser_password = 'DB PASSWORD'
```
