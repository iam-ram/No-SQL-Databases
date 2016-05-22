#Install MongoDB

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | sudo tee /etc/apt/sources.list.d/mongodb.list
sudo apt-get update
sudo apt-get install -y mongodb-org


sudo service mongod start
sudo service mongod status
sudo service mongod stop
sudo service mongod restart


Note:
	* Mongo DB default port: 27017
	* MongoDB starts automatically after install
	* Stop MongoDB to modify the conf file to allow mongo db to listen to all ports.
	* sudo vi /etc/mongod.conf
	* # Listen to local interface only. Comment out to listen on all interfaces. 
	  # bind_ip = 127.0.0.1


Py Mongo:
1) sudo pip install pymongo

Start Client:
1) cd to MongoDB/client folder.
2) config.json: Verify and modify the IP and port as per the server connections.
3) run : $python PeerBenchmark.py -c config.json -i 100000 -e 200000

	$ python PeerBenchmark.py [-h] -c CONFIG -i INDEX -e END

		Standard Arguments for talking to Distributed Index Server

		optional arguments:
			  -h, --help            show this help message and exit
			  -c CONFIG, --config CONFIG
			                        Config file of the network
			  -i INDEX, --index INDEX
			                        key range start index
			  -e END, --end END     
						key range end index
		Note:	* All arugment is mandatory.
or
4) chmod +x benchmark.sh
5) run : $./bechmark.sh