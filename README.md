node-red-node-thingrest
=====================

A <a href="http://nodered.org" target="_new">Node-RED</a> node to talk to <a href="http://www.thingworx.com" target="_new">ThingWorx</a> using HTTP REST protocol.

Install
-------

Run the following command in the root directory of your Node-RED install, usually
this is ~/.node-red .

        npm install node-red-node-thingrest

        or direct from github at

        npm install git+https://git@github.com/obiwan314/node-red-node-thingrest.git


Usage
-----

Provides a single node - It accepts a msg.payload containing an object whose property names will be applied to the Thing the node is configured for.

###Input

This node acts as an output node. It expects to receive an msg object with a property of payload that maps directly to the Thing you are trying to update.

**Example**:

If the Thing you are trying to update has a String property called stringProperty and a Number property called numberProperty, the following payload would  update these property values.

msg.payload = {
	stringProperty:"Hello World",
	numberProperty:345	
};

The node contains a property, ThingName, which can be set when it is created. ThingName can be overridden by providing a msg.thingName property along with your payload.

Below is a simple example flow:

![Node-RED: A visual tool for wiring the Internet of Things](http://nodered.org/images/node-red-screenshot.png)

