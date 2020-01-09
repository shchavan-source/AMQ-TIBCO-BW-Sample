# TIBCO Sample code for AMQ Connection
## TestHAFlipPublisher_no_correlation will produce messages on AMQ broker
## TestHAFlipSubscriber_no_correlation will consume messages from AMQ broker

**TIBCO BW Designer is required to execute these samples**

###### TestHAFlipPublisher_no_correlation

**Following are the set of GV that can be used to configure the producer**

`AMQ/LOG_URL: AMQ Broker URL`
`AMQ/SOI_URL: AMQ Broker URL`
`AMQ/Password: Password for the amqapps user`
`AMQ/LOG_Pswd: Password for the amqapps user`
`Config/Iteration: Number of messages to be produced`
`Config/QRequestorQ: Queue name where the JMS Queue Requestor activity will push the messages`
`Config/QRequestorResQ: Queue name where the JMS Queue Requestor activity will be waiting to get the response`
`Config/ReqQueue: Queue name where the JMS Queue Sender will produce messages`
`Config/ResQueue: Queue name where the JMS Queue Reciever will recieve messages`
`Config/Sleep: Sleep interval in milliseconds after sending a message`

Go to the Shared/AppConnection and Shared/LogConnection and perform Test Connection to test if the application is able to make connection.

To start the execution of the program, start the Processes/MessageWatcher. This process will start publishing messages on the AMQ Broker.

###### TestHAFlipSubscriber_no_correlation

**Following are the set of GV that can be used to configure the producer**

`AMQ/LOG_URL: AMQ Broker URL`
`AMQ/SOI_URL: AMQ Broker URL`
`AMQ/Password: Password for the amqapps user`
`AMQ/LOG_Pswd: Password for the amqapps user`
`Config/QRequestorQ: Queue name where the JMS Queue Requestor activity will push the messages`
`Config/QRequestorResQ: Queue name where the JMS Queue Requestor activity will be waiting to get the response`
`Config/ReqQueue: Queue name where the JMS Queue Sender will produce messages`
`Config/ResQueue: Queue name where the JMS Queue Reciever will recieve messages`

Go to the Shared/AppConnection and Shared/LogConnection and perform Test Connection to test if the application is able to make connection.

To start the execution of the program, start the Processes/EndpointReceiver and Processes/EndpointReceiver-QueueRequestor. This process will start publishing messages on the AMQ Broker.
