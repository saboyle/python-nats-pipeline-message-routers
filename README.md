# python-nats-pipeline-message-routers
Exploratory project implementing different types of message router (incl content and context)

## Content Based Routing [EIP p230]
* A simulation client randomly orders a product at a random time interval. The client submits orders to an 
order queue. 
* A content based router listens to the order queue and forwards the orders to either product specific queues for
high volume products or a general queue for all others.
* Workers listen to the product queues and print the orders (wiretaps).

## Distribution using consistent hashing (future)
* A simulation client randomly orders a product at a random time interval.  The client submits orders to an 
order queue.
* A content router uses a consistent hashing function to distribute the orders to N queues.
* Workers listen to the product queues and print the orders (wiretaps).

## Distribution using dynamic routing [EIP p244]
* A simulation client randomly orders a product at a random time interval.  The client submits orders to an 
order queue.
* A content router uses a configuration store to distribute the orders to N queues.
* Workers listen to the product queues and print the orders (wiretaps).
* Each time a worker is added it updates the configuration store to notify the dynamic router that it can receive 
messages matching a specific pattern.


## Objectives
* Implement basic content based message router [EIP p78]
* Extend to explore consistent hashing to distribute to work queues
* Explore pro's and con's of hard-coded hashing functions for scaling / distribution
* Follow on - Distributed Hash Ring

## Refs

### Consistent Hashing
* http://michaelnielsen.org/blog/consistent-hashing/
* https://arxiv.org/pdf/1406.2294.pdf (Jump Consistent Hashing)
