# Kinesis Video Streams(KVS)

### What is KVS?
1. Kinesis Video Streams automatically provisions and elastically
scales all the infrastructure needed to ingest streaming video 
data from millions of devices.

2. Benefits 
	- Stream video from millions of devices
	- Connect and stream from millions of devices
	- Build real-time vision and video-enabled apps
	- Playback live and recorded video streams
	- Build apps with two-way, real-time media streaming
	- Secure
	- Durable, searchable storage
	- No infrastructure to manage

3. Workflow

	``camera -> KVS -> data analysis tool or AI``

4. Use cases 
	- smart home 
	- smart city 
	- Industrial automation 

### Dev Guide
1. Kinesis Video Streams API 
	- Producer API: Kinesis Video Streams provides a PutMedia
	API to write media data to a Kinesis video stream. In a 
	PutMedia request, the producer sends a stream of media 
	fragments. A fragment is a self-contained sequence of 
	frames.
	
	- Consumer APIs: The following APIs enable consumers to 
	get data from a stream. 
2. run with docker: 
	``sudo docker run -it --network="host" 546150905175.dkr.ecr.us-west-2.amazonaws.com/kinesis-video-producer-sdk-cpp-amazon-linux /bin/bash``

### RSTP 
1. The Real Time Streaming Protocol is a network control protocol 
   designed for use in entertainment and communications systems
   to control streaming media servers.    
2. 

