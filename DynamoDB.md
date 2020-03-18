# Dynamo: Amazon's highly Available Key-value Store 

General terms: 
  - Algorithms, Managemnt, Measurement, Perfomance, Design 
  
### 1. Background 
1. traditional relation database drawbacks: 
    mostly primary keys, do not require complex queries. 
    these opertions are expensive in terms of physical devices and human labors. 
    it is not easy to scale or partitioning schemes for load balancing 
2. Dynamo has a simple scheme of key/vlue interface. 

### Create a NoSQL table by console 
1. Key differences 
	- The Partition Key is responsible for data distribution across your nodes.
	- The Clustering Key is responsible for data sorting within the partition.
	- The Primary Key is equivalent to the Partition Key in a single-field-key table (i.e. Simple).
	- The Composite/Compound Key is just any multiple-column key
2. Query the table by the console 
	- [table] Music, Artist, SongTitle 

3. Select a row to peform actions such deletion. 

### TTL 
1. Time to Live (TTL) for Amazon DynamoDB lets you define when
	items in a table expire so that they can be automatically 
	deleted from the database. With TTL enabled on a table, you 
	can set a timestamp for deletion on a per-item basis, 
	allowing you to limit storage usage to only those records that are relevant.
2. Unix time system, a number (in epoch time format)

3. enable time to love(live) by console 

Steps:
	``
	1. sign in the console 
	2. choose tables 
	3. in Table details, net to TTL attribute, choose
		manage TTL 
	4. then, enter TTL attribute name: name for TTL 
	``
4. enable a TTL Example table by command line: 
	``
	aws dynamodb update-time-to-live --table-name TTLExample --time-to-live-specification "Enabled=true, AttributeName=ttl"
	``
5. describle TTL on the TTLExample table
	``
	aws dynamodb describe-time-to-live --table-name TTLExample
	``
6. Add time extension 
	``
	EXP=`date -d '+5 days' +%s`
	aws dynamodb put-item --table-name "TTLExample" --item '{"id": {"N": "1"}, "ttl": {"N": "'$EXP'"}}'
	``



	





