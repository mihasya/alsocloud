<!SLIDE title-slide>

## Building a cloud service on a cloud infrastructure at

<img src="sg.png" height="109" />

### Also, cloud.

Mikhail Panchenko, Surge 2011
<!SLIDE bullets>

* Who am I?
  * Pancakes
  * Infrastructure Engineer at SimpleGeo
  * Backend Engineer at Flickr before that
  * Backend and Frontend Engineer at Yahoo! Ops/Tools before that
  * Philosophy, Economics, and French major before that

* ____ 
  * @mihasya
  * pancakes@simplegeo.com


<!SLIDE bullets>

* <img src="sg.png" height="109"/>
  * Tools for developers
  * Primarily focused on services, some data-oriented APIs
  * PaaS? \*aaS, who gives a @%$#
  * Availability, redundancy part of brand
  * No pressure
<!SLIDE fixed-top>

# Agenda
* Goals
* A little bit of theory
* Architecture
* Challenges (read: The Cloud)
* What works and what doesn't

<!SLIDE>

## Architectural Goals
* High availability
* Linear scalability
* Elasticity
* Redundancy/Fault Tolerance

<!SLIDE>

# Sound Familiar?

<!SLIDE>

# Some Theory, Food for Thought

<!SLIDE>

# The Internets as Complex Systems

<!SLIDE>

# TODO: cover of Normal Accidents

<!SLIDE quotation>

__Complex interactions__ are those of unfamiliar sequences, or unplanned and unexpected sequences, and either not visible or not immediately comprehensible. 

<p class="credit">Charles Perrow. Normal Accidents: Living with High-Risk Technologies (p. 78). Kindle Edition.</p>

<!SLIDEi quotation>

"The notion of baffling interactions is increasingly familiar to all of us. It characterizes our social and political world as well as our technological and industrial world. As systems grow in size and in the number of diverse functions they serve, and are built to function in ever more hostile environments, increasing their ties to other systems, they experience more and more incomprehensible or unexpected interactions. They become more vulnerable to unavoidable system accidents."

<p class="credit">Charles Perrow. Normal Accidents: Living with High-Risk Technologies (p. 72). Kindle Edition.</p>

<!SLIDE quotation>
"The beauty of this is its simplicity. Once a plan gets too complex, everything can go wrong."
<p class="credit">Walter Sobchak, <em>The Big Lebowski</em></p>
<!SLIDE>

# The Birds 'n' the Bees

<!SLIDE fixed-top>
## Write Path
<img src="birdsnbees1.png" height="501px"/>

<!SLIDE fixed-top>
## Cassandra
  * Homogenous distributed model
  * Random load distribution
  * A mostly-textbook DHT
  * Generally well understood by developers
  * A perfect foundation for our architecture (we'll get back to this)

<!SLIDE fixed-top>
## RabbitMQ
  * Definitely a grenade for our knife-fight
  * Very high throughput, both in and out
  * Lots of concurrent connections/consumers
  * 2.x bulletproof - no stability issues
  * Disk persistor - well understood degradation


