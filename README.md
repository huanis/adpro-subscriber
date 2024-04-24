## AMQP
Advanced Message Queuing Protocol is a protocol that allows end-to-end communication by sending and receiving messages with the use of a message broker vendor/platform. Depending on the rules defined and the routing key provided in the message, the message is distributed to different queues. The message will be consumed by a subscriber from the queue.

"amqp://guest:guest@localhost:5672"
- amqp: refers to the fact the protocol used, which is the Advanced Message Queueing Protocol
- guest (the first one): the username to connect to the queue
- guest (the second one): the password to connect to the queue
- localhost: where the queue is deployed/running
- 5672: the port used to connect to the queue in the localhost