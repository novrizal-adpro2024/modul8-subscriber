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

**d. Reflection and Running at least three subscribers.**

![CMD](https://cdn.discordapp.com/attachments/1111642397248598067/1231985612823724042/image.png?ex=6638f303&is=66267e03&hm=f76a97f4c27058d0c3b96bf3d4b7c77b274c92dadb8c803610a15bbeea0c1eea&)
In the picture above, it shows that I tried to run 3 subscriber consoles in one time. 
As a result, the event processing is splited, each of them were processing different one.

![Chart 3 Subs](https://cdn.discordapp.com/attachments/1111642397248598067/1231985841530994758/image.png?ex=6627cfb9&is=66267e39&hm=34d106f71f82a4cc7305ec276b09fe9d189eed98632030f4613e0ffe415d3f89&)
In the graph above, we can see the difference (when i used only 1 console). 
The current queued messages are decreased. It happens because message are being consumed paralleled by 3 subscribers.
As a result, this will decrease the queued message & improving the consuming process' speed.