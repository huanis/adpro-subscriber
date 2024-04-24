## AMQP
Advanced Message Queuing Protocol is a protocol that allows end-to-end communication by sending and receiving messages with the use of a message broker vendor/platform. Depending on the rules defined and the routing key provided in the message, the message is distributed to different queues. The message will be consumed by a subscriber from the queue.

"amqp://guest:guest@localhost:5672"
- amqp: refers to the fact the protocol used, which is the Advanced Message Queueing Protocol
- guest (the first one): the username to connect to the queue
- guest (the second one): the password to connect to the queue
- localhost: where the queue is deployed/running
- 5672: the port used to connect to the queue in the localhost


![rabbitmq](image-4.png)
The image above shows when the rate of message sent by publisher is faster than the rate of messages acknowledged by the consumer.

![consoles](image.png)
The image above shows that I am running 3 subscribers for 1 publisher. As you can see, one message only goes to one subscriber. The publisher published 5 messages in total. One of the subscriber got 3 of them, one got 2, and one got only 1.

![last](image-1.png)
The image above shows there are 13 messages in the queue in total. This is because although the subscribers are many, the rate in which they consume the messages are not enough to match the rate of messages sent by the publisher.