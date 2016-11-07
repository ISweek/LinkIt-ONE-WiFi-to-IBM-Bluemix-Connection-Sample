# LinkIt-ONE-WiFi-to-IBM-Bluemix-Connection-Sample
This repository contains the quickstart and registered device sample, and contains samples for connecting LinkIt ONE devices to the IBM Internet of Things Foundation The events that are emitted in this sample are: • Internal sensor temperature &amp; humidity

<h1>Pre-requisite setup for the 2 flows</h1>
<ol>
  <li> Connect LinkIt ONE board to the work station ( laptop /desktop )</li>
  <li> Install sketch on desktop / laptop</li>
  <li> Download knolleary client library for the Arduino, from this link <a href="https://github.com/knolleary/pubsubclient">https://github.com/knolleary/pubsubclient</a><br />
    In the sketch, to load it into the Arduino IDE, Select Sketch -&gt;   Import Library -&gt; Add Library and select the folder which contains   PubSubClient.cpp and PubSubClient.h files.</li>
  <li> Connect the USB cable to the LinkIt ONE and other end to desktop / laptop which has the sketch installed on it</li>
  <li> Connect temperature and humidity sensor to the LinkIt ONE board.   The sample code assume that the sensor has been connected to the D2 PIN   of the LinkIt ONE board.</li>
  <li> The samples folder of this repository (<a href="https://github.com/iotgeek/LinkItONE-IBMBluemix/">https://github.com/iotgeek/LinkItONE-IBMBluemix/</a>) contains 2 examples,   a) Quickstart flow –quickstart.ino   b) Registered flow – registereduser.ino</li>
  <li> Compile the 2 sketch codes (corresponding to the flows)</li>
  <li> Depending upon the requirement, push one of the flows to the  LinkIt ONE board</li>
</ol>
<h1> Quickstart flow</h1>
<ol>
  <li> Modify the WIFI_AP, WIFI_PASSWORD &amp; WIFI_AUTH values to your Wifi AP name, password and security type .</li>
  <li> Modify the macstr  with the MAC Address of the LinkIt ONE,   compile and upload to the LinkIt ONE board. Now the device should be   ready to send temperature and humidity data to the IBM Bluemix cloud.</li>
  <li> Open the quickstart dashboard from browser (<a href="http://quickstart.internetofthings.ibmcloud.com/#/">http://quickstart.internetofthings.ibmcloud.com/#/</a>)</li>
  <li> Provide the MAC Address (in case of the example, its &ldquo;aabbccddeeff&rdquo;) in the textbox &quot;Ready to View data?&quot;</li>
  <li> You can see the graph with temperature and humidity details.</li>
</ol>
<h1>Registered Flow</h1>
<ol>
  <li> Modify the WIFI_AP, WIFI_PASSWORD &amp; WIFI_AUTH values to your Wifi AP name, password and type of encryption.</li>
  <li> Modify the servername , clientName  and password  in the sketch code</li>
  <li> Modify the macstr  with the MAC Address of the device, compile and upload to the LinkIt ONE board</li>
  <li> Modify the servername, in the sketch code, by providing the   values in the following format   &quot;666666.messaging.internetofthings.ibmcloud.com&quot;, by replacing &quot;666666&quot;   with your organization</li>
  <li> Modify the clientName  , in the sketch code, by providing the   values in the following format &quot;d:666666: LinkItONE: aabbccddeeff &quot;, by   replacing &quot; aabbccddeeff &quot; with the MAC Address , &quot;666666&quot; with the   organization and LinkItONE by device type.</li>
</ol>
<h1>Development</h1>
<p>•   The code contains comments, which explains how to modify the parameters<br />
  •   In case of registered flow, you will have to connect to <a href="https://internetofthings.ibmcloud.com/dashboard/#/">https://internetofthings.ibmcloud.com/dashboard/#/</a> and create the     following<br />
  •   Organization<br />
  •   Device<br />
  •   Auth tokens </p>
