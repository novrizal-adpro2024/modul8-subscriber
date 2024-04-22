# Module 8: Software Architecture

> #### Novrizal Airsyahputra - 2206081780 - Advance Programming B

---

### Reflection

**a. what is amqp?**

**ANS:**
AMQP (Advanced Message Queuing Protocol) is an open standard application layer protocol for message-oriented middleware.
AMQP provides a method for systems to communicate with each other in a robust and reliable manner. 
AMQP is designed to support messaging between applications or components in a distributed system, 
allowing for the asynchronous exchange of messages.


**b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for?**

**ANS:**

guest:guest@localhost:5672 indicates connecting to the AMQP server running locally with the username and password set to guest, using the default port 5672.
In the guest:guest@localhost:5672, each part represents different components of connecting to an AMQP server:

- guest:guest: It is the username and password combination. In this case, the username & the password are both guest. 
These are default credentials often used for local development or testing purposes.

- localhost:5672: It represents the host and port of the AMQP server. localhost means the server is running on the local machine
and 5672 is the default port number for AMQP communication.

**c. Simulation slow subscriber.**

![Chart Slow RabbitMQ](https://cdn.discordapp.com/attachments/1111642397248598067/1231982620850524322/image.png?ex=6638f039&is=66267b39&hm=6a8f131ab69691b6035307050c48c7569ec132b23bd1b94c072d58f3faa71e67&)

In the graph above, I have rapidly executed the publisher 6 times, evidenced by the queued messages totaling 30. 
This means that there are 30 messages in the queue awaiting consumption by the subscriber.