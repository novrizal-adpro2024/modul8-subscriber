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