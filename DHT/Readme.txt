#Simple Distributed Hash Table (DHT):

Start DHT Server:
1) Change directory to DHT/Benchmark
2) run: $python serverthread.py -c config.json -s 3340

	$ python serverthread.py [-h] -c CONFIG -s SERVER

		Standard Arguments for talking to Distributed Index Server

		optional arguments:
			  -h, --help            show this help message and exit
			  -c CONFIG, --config CONFIG
                        			Config file of the network
			  -s SERVER, --server SERVER
			                        Server Port Number
									
		Note: * arugment -c and -s is mandatory
or
3) chmod +x benchmarkserver.sh
4) run : $./benchmarkserver.sh
Start Client:
1) cd to DHT/Benchmark folder.
2) config.json: Verify and modify the IP and port as per the server connections.
3) run : $python clientthread.py -c config.json -i 100000 -e 200000

	$ python clientthread.py [-h] -c CONFIG -i INDEX -e END

		Standard Arguments for talking to Distributed Index Server

		optional arguments:
			  -h, --help            show this help message and exit
			  -c CONFIG, --config CONFIG
			                        Config file of the network
			  -i INDEX, --index INDEX
			                        key range start index
			  -e END, --end END     
						key range end index
	
or
4) chmod +x benchmarkpeer.sh
5) run : $./benchmarkpeer.sh
