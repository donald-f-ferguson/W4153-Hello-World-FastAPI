# W4153-Hello-World-FastAPI

## Overview

Simple Hello World FastAPI to help students get their first VM deployed on a cloud.

## Execution

### AWS Instance

- Create a "free tier" compatible instance.
- Make sure you setup free tier alerting emails.
- I chose Ubuntu Linux.
- You can use the default VPC but create a new security group.
- Make sure you enable remote access.
- Create a new key pair and save the .pem file somewhere safe.
- When EC2 instance is running, connect to it by selecting the instance and then
the connect menu option. Use the default connection manager.

### Running Application

- I used Ubuntu OS on Amazon instance.
- Some commands:
```
sudo apt update

sudo apt install python3 python3-pip -y

git clonehttps://github.com/donald-f-ferguson/W4153-Hello-World-FastAPI.git

sudo apt install python3.12-venv

sudo python3 -m venv ./venv

source venv/bin/activate

pip install requirements.txt

python main.py &

curl localhost:8000

```
- And you should get ...
```
INFO:     127.0.0.1:35572 - "GET / HTTP/1.1" 200 OK
{"\n\nmessage":"Hello from W4153-Hello-World-FastAPI!\n\n"}(venv)
```

### Remote Access

- Navigate to the security group.
- Add an inbound rule for TCP, port 8000 and 0.0.0.0/0

<img src="inbound-rules.jpg">

- Go back to EC2 instance configuration and get public IP address.
- Mine was 53.208.146.60
- Navigate to http://54.208.146.60:8000/ (__Make sure you use HTTP. Browser default to HTTPS.__)

# Finish

- Shutdown and terminate your instance.
- We can make another one later.






