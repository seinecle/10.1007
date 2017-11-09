= Definition of IoT and connected objects
Clément Levallois <levallois@em-lyon.com>
2017-08-01

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:

:title-logo-image: EMLyon_logo_corp.png[align="center"]

[.stretch]
image::EMLyon_logo_corp.png[align="center"]

==  'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

==  Internet of Things, connected objects?

==  !
[quote, Wikipedia, entry "Internet of Things" visited on 2017/08/01]
________________________________________
The Internet of things (IoT) is the inter-networking of physical devices, vehicles (also referred to as "connected devices" and "smart devices"), buildings, and other items embedded with electronics, software, sensors, actuators, and network connectivity which enable these objects to collect and exchange data.
________________________________________

==  !
Some comments on this definition:

- we are familiar with Internet used to transmit information from computer to computer (sending an email, visiting a web page...)
- the expression "Internet of things" insists on a different kind of use: what if we could connect any object (not just our computers or smartphones) to the Internet?

The idea to connect objects to the Internet is not new: professors connected a Coke Machine to Internet in the late 1970s or early 1980s, so that they could check from their computers if it was empty or not.footnote:[https://www.cs.cmu.edu/~coke/history_long.txt]

==  !
Once we understand what is the "Internet of things", the meaning of "connected objects" is clear: these are the objects connected to this network.

==  !
[NOTE]
====
*What about "smart objects?".*

This is synonymous to connected objects, where "smart" insists that the object can have a richer set of functions thanks to being connected to the Internet.
For example a "smart car" is a car that can http://www.trustedreviews.com/news/over-the-air-software-update-makes-the-tesla-p85d-even-faster-2924452[drive faster] a month after your purchased it, thanks to updates made to its software through the Internet.
====

==  !
Starting in the 2000s, we moved from small, fun experiments to the development of an entire industry based on this concept of connecting things to the Internet.

With _decreasing costs_ for creating connecting objects, and easier protocols to connect (like Wifi, bluetooth and others, which appeared in the late 1990s), connected objects started to become interesting playground for serious innovation.

What kind of new service could be created with them? What value would they bring?



==  !
==  Examples

==  !
Connected objects are more and more present in our lives. We can put them in 2 categories:

==  !
==== 1. connected objects for consumers

==  !
https://explore.garmin.com/en-US/vivo-fitness[a wrist band], or the https://www.amazon.com/dp/product/B00X4WHP5E/ref=EchoCP_dt_tile_text[Amazon Echo], which is a sound speaker doubling as a Digital Assistant. Or a scale by https://health.nokia.com/fr/fr/body[Nokia], which tracks your weight but also pulsations.

[.stretch]
image::garmin.png[align="center", title="source: https://explore.garmin.com/en-US/vivo-fitness"]


==  !
TIP: Connected objects we can dress with are called *wearables* (https://www.cnet.com/topics/wearable-tech/best-wearable-tech/[smart watches and fitness trackers mostly], but https://www.wareable.com/smart-clothing/best-smart-clothing[actual clothing as well])

TIP: Connected objects for domestic use are often called *smart house devices*, and include thermostats, cameras and https://www.postscapes.com/internet-of-things-award/connected-home-products/[more].


==  !
==== 2. connected objects for the industry

==  !
Connected objects are useful to help keep track of all pieces of material and semi-finished products along the production line, in all industries (from agriculture to manufacturing, through health care etc.)

The goal is to eliminate waste and increase speed by controlling and monitoring their processes more closely thanks to these devices.

==  !
[#img-industry-device]
.This device can send temperature measurement and many other kinds to a monitoring console
[link=http://embedded-computing.com/news/wzzard-intelligent-sensing-platform-brings-smart-mesh-networking-to-iot-edge-applications/]
[.stretch]
image::industry-sensor.jpeg[align="center"]

Examples of companies managing IoT for the industry are http://www.ripplesiot.com/[Ripples], http://www.pentaho.com/internet-of-things-analytics[Pentaho], or https://www.ptc.com/en/internet-of-things[PTC].

==  !
In service industries, connected objects help deliver the service better (like https://disneyworld.disney.go.com/plan/my-disney-experience/bands-cards/[the MagicBand at Disney World]), and help control the quality of the service delivered by taking measures.

==  !
[.stretch]
image::magicband.jpg[title="The \"MagicBand\" by Disney which acts as an entrance ticket and e-wallet"]

==  The anatomy of a connected object

==  !
What makes an object part of the Internet of things? 3 things:

==  !
==== 1. The object must be connected (duh)

==  !
The connection can take many forms:

==  !
[start=1]
a. the object can receive and send data, like this Thermostat:

==  !
.The Nest thermostat
[link=https://nest.com/thermostat/meet-nest-thermostat/]
[.stretch]
image::nest.jpg[align="center"]

==  !
The thermostat  sends temperature measurements to your smartphone, and receives instructions from you (to decrease or increase the temperature).

==  !
[start=2]
b. The object can be just an emitter

==  !
A connected object can just broadcast some information without receiving anything. Two cases:

==  !
- the object sends data automatically, like these connected beehives build by http://scontent.cdninstagram.com/t51.2885-15/s480x480/e35/c19.0.1041.1041/14723479_163242737474300_6697748361329508352_n.jpg[emlyon students] and now producing honey https://makersbeehives.herokuapp.com/[on the roof of the school]. They send pictures / temperature measures:

[.stretch]
image::bees.gif[align="center"]

== !
If the object is sending data, it supposes it has a *sensor* to measure things around it, so that it can then send this measure.
Sensors are pieces of electronic equipment, often quite tiny.
The list of sensors is immense and this is just a small sample:

== !

.Sensors!
[link=https://www.sparkfun.com/categories/305?filter_option%5Bprice%5D%5B%5D=is_price_range_0_10&filter_option%5Bprice%5D%5B%5D=is_price_range_10_20&filter_price_floor=&filter_price_ceil=]
[.stretch]
image::sensors.jpg[align="center"]

==  !
- or the object sends a signal continuously, which is received by your phone when you walk next to it. In this case the object is called a *beacon*.
It is used in stores to interact with shoppers:

[.stretch]
image::iBeacon.jpg[align="center"]

==  !
And it is also used in logistics to track shipping items:

video::Q5VDEdF3cBc[youtube]

==  !
[start=3]
c. The object can be just a receiver

==  !
In this case, the connected object can display some information that it receives from the network it is connected to.

This is the kind of objects we are going to build in this course: an object which receives data about air pollution, and shows it on a screen.
Check the small screen in the middle of it!

==  !
[.stretch]
image::object.jpg[align="center"]

==  !
[NOTE]
====
Connected objects which receive data can do many things with it, not just showing stuff on screen.

The connected object can move, compute things, make sound or light... everything is possible.
====

==  !
[start=4]
d. also interesting: the object can connect... to another object

This is called a "swarm": when multiple objects can coordinate their actions by connecting with each other, instead of connected separately to a central point.

Connected objects can coordinate to move together and perform a common action (like https://www.youtube.com/watch?v=CJOubyiITsE[moving a child!]), or just exchange data.

==  !

==  The end


==  !
Find references for this lesson, and other lessons, https://seinecle.github.io/IoT4Entrepreneurs/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
pass:[    <!-- Start of StatCounter Code for Default Guide -->
    <script type="text/javascript">
        var sc_project = 11410058;
        var sc_invisible = 1;
        var sc_security = "11410058";
        var scJsHost = (("https:" == document.location.protocol) ?
            "https://secure." : "http://www.");
        document.write("<sc" + "ript type='text/javascript' src='" +
            scJsHost +
            "statcounter.com/counter/counter.js'></" + "script>");
    </script>
    <noscript><div class="statcounter"><a title="site stats"
    href="http://statcounter.com/" target="_blank"><img
    class="statcounter"
    src="//c.statcounter.com/11410058/0/11410058/1/" alt="site
    stats"></a></div></noscript>
    <!-- End of StatCounter Code for Default Guide -->]
