#Download Install and Benchmark Redis:

1. Redis installation

sudo apt-get update

sudo apt-get install build-essential

sudo apt-get install tcl8.5

wget http://download.redis.io/releases/redis-stable.tar.gz

tar xzf redis-stable.tar.gz

cd redis-stable

make

make test

sudo make install

cd utils

sudo ./install_server.sh

2. Start Redis

Default port is set to 6379 in redis. it can be changed during config. I am using 7555

sudo service redis_7555 start
sudo service redis_7555 stop

3. Python Client:

$ sudo pip install redis

Start Client:
1) cd to Redis/client folder.
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
