# mqmeter
MQ Jmeter Extension.

A [JMeter](http://jmeter.apache.org/) Plugin to put message on [IBM MQ](https://www.ibm.com/products/mq) queue. It connect to MQ Server through server channel with ip address and port number, also with userID that has the rights to put message on queue.


## Install

Build the extension:

    mvn package

Install the extension `mqmeter-x.y.z.jar` into 

    `$JMETER_HOME/lib/ext`.

## Usage

After installing `mqmeter`, add a Java Request Sampler and select the `MQClientSampler`
class name. The following properties are required.

* **mq_manager**: MQ Maneger name. You can find it through IBM WebSphere MQ Explore or console.
* **mq_queue**: MQ Queue name. Could be Local or Remote queue.
* **mq_hostname**: Host name or ip address where MQ Server is running.
* **mq_port**: Port number of the MQ Server listener.
* **mq_channel**: The Server channel name on MQ Server.
* **mq_user_id**: The userID with rights to connect and add message on queue.
* **mq_message**: The content of the message that you want.


![Screenshot](https://github.com/JoseLuisSR/img2/blob/master/mqmeter/JavaRequestSampler.png)


## IBM WebSphere MQ

The below images show where find the values for some of the above properties

* **MQ Manager**

![Screenshot](https://github.com/JoseLuisSR/img2/blob/master/mqmeter/MQManager.png)

* **MQ Server channel**

![Screenshot](https://github.com/JoseLuisSR/img2/blob/master/mqmeter/MQServerChanel.png)

* **MQ Server listener**

![Screenshot](https://github.com/JoseLuisSR/img2/blob/master/mqmeter/MQServerListener.png)

* **MQ Chlauth**

You can find the steps to add users access to MQ Manager through Channel Authentication (Chlauth) with this tutorial 
[IBM CHLAUTH](http://www-01.ibm.com/support/docview.wss?uid=swg27041997&aid=1)

![Screenshot](https://github.com/JoseLuisSR/img2/blob/master/mqmeter/MQChlauth.png)