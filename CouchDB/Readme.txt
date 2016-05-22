#Install CouchDB

sudo apt-get update
sudo apt-get install couchdb -y

sudo start couchdb
sudo stop couchdb

Note:
	* Couch DB default port: 5984
	* sudo pip install httplib2
	* Create db named: benchmark in CouchDB: curl -x PUT http://<server_ip>:5984/benchmark


Py CouchDB:

Start Client:
1) cd to CouchDB/client folder.
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
5) run : $./benchmark.sh