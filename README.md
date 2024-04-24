### Understanding publisher and message broker

#### a. How many data your publisher program will send to the message broker in one run?

Based on the code in the main function of the publisher program, the publisher program should send five (5) messages to the message broker in one run. Every one of the messages here is an instance of UserCreatedEventMessage struct with different user_id (from 1 to 5) and user_name values.

#### The URL "amqp://guest:guest@localhost:5672" is the same as in the subscriber program. What does it mean?

The URL "amqp://guest:guest@localhost:5672" is the URL used to establish a connection with the AMQP message broker. It specifies the protocol (AMQP), authentication credentials (guest:guest), and the host and port where the message broker is running (localhost:5672).

The fact that the same URL is used in both the publisher and subscriber ( or listener) programs means they have to connect to the same message broker instance. What should happen here is the publisher sends messages to the broker and the subscriber or the listener receives those messages from the same broker.