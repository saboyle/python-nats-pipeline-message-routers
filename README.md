# python-nats-pipeline-message-routers
Exploratory project implementing different types of message router (incl content and context)

## Objectives
* Implement basic content based message router [EIP p78]
* Extend to explore consistent hashing to distribute to work queues
* Explore pro's and con's of hard-coded hashing functions for scaling / distribution
* Follow on - Distributed Hash Ring

## Refs
### Consistent Hashing
* http://michaelnielsen.org/blog/consistent-hashing/
* https://arxiv.org/pdf/1406.2294.pdf (Jump Consistent Hashing)
