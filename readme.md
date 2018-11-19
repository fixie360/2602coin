Flask 0.12.2
requests 2.18.4

This is a Docker implementation of a simple crypto coin. Using python and flask.

To start docker environment:

	Build the node and client images:
		1. Navigate to 2602coin_base directory
		2. $ docker build -t 2602coin_base .
		3. Navigate to 2602coin_client directory
		4. $ docker build -t 2602coin_client .

	Run the containers:
		1. $ docker run -d -p 80:2602 --name 2602coin_node1 2602coin_base
		2. $ docker run -d -p 8080:8080 --name 2602coin_client1 2602coin_client

	For multiple nodes increment the public port and container name, for example:
		1. $ docker run -d -p 81:2602 --name 2602coin_node2 2602coin_base

	For multiple clients increment the public port and container name, for example:
		1. $ docker run -d -p 8080:8080 --name 2602coin_client1 2602coin_client

To access the flask apps, enter your docker host machine's IP address followed by the public port of the app you're targeting (e.g. 192.168.99.100:80)
