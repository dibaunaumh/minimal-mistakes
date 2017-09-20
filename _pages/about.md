---
title: "About"
layout: single
permalink: /about
date: 2017-09-20T00:07:00-00:00
sidebar:
  nav: "about_docs"

matrix_browser:
  - image_path: /assets/images/screenshot1.png
    alt: "Organized Space"
  - image_path: /assets/images/screenshot3.png
    alt: "Raw feed"
  - image_path: /assets/images/screenshot2.png
    alt: "Service providers buildings"


matrix_cloud:
  - image_path: /assets/images/access2.png
    alt: "Buildings"
  - image_path: /assets/images/access1.png
    alt: "Composite building"
  - image_path: /assets/images/access3.png
    alt: "Building servers"

matrix_hovercraft:
  - image_path: /assets/images/processing1.png
    alt: "Resident hackers"
  - image_path: /assets/images/processing3.png
    alt: "Processing flow"
  - image_path: /assets/images/processing2.png
    alt: "Hovercraft powering resident hackeres & data-pipes"

---


## Access model
A new uniform way to access information & data
{% include feature_row id="matrix_cloud"%}

<h3>The problem</h3>
<ul>
  <li>There are millions of data-islands across the Web, & each one of them has its own way of accessing the data & making sense of it.</li>
  <li>This means that you need extensive manual work to be able to connect to, understand, & normalize each data source, & only then can you start processing, aggregating & merging it with other data sources.</li>
  <li>Furthermore, the process of discovering the available data islands & comparing them is also a laborious manual work.</li>
  <li>There were many efforts to add semantic layers over the Web & link data across islands, but so far none of them has proved effective in solving this problem.</li>
</ul>
<h3>Solution overview</h3>
<ul>
  <li>The Web Wide Matrix offers a completely new access model to the information & data across the web, allowing simple uniform access to any data island</li>
  <li>This access model also takes into account that the data continuously evolves & updates, so the way you consume it isn't by taking a snapshot or run some query at one point in time, but rather by subscribing to the stream of updates</li>
  <li>Another powerful feature of the model is that you get an overview of the available data sources & can easily compare them & discover the data that you want</li>
</ul>
<h3>The model</h3>
<ul>
  <li>In the real-world, you have maps for organizing & discovering the available resources. If you need to buy some product, you look up the address of a store that sells it, & then go to that address to buy the product</li>
  <li>Similarly, within a place you have maps that help you find the exact item that you want</li>
  <li>The Web Wide Matrix is an abstraction layer over the Web, based on a spatial model similar to the real-world</li>
  <li>It is based on the concept of Composite Buildings, for storing data</li>
  <li>It starts with the ground level, on which you can have buildings, whose address is their coordinates</li>
  <li>Each building contain metadata & a payload of data
    <ul>
        <li>If it's just one piece of data, e.g., a JSON document, the building is called "atomic building"</li>
    </ul>
  </li>
  <li>The building can also have floors, which also contain data - for example if  there's a newer version of the data, it will be available in a new floor</li>
  <li>But buildings can also have nested buildings inside them, whose address is based on their coordinates on the floor in which they are located
    <ul>
      <li>Such buildings are called: "composite buildings"</li>
    </ul>
  </li>
  <li>In addition, floors within buildings can be divided into areas, called Rooms, for grouping related data together</li>
  <li>The way buildings are connected to the Web is using special "data-pipes" that continuously stream data from some data-source on the Web into a building</li>
  <li>The content of buildings is following a common machine understandable format, so you can access & process all data in a uniform way</li>
</ul>

## Processing model
A mechanism for easily processing & aggregating data
{% include feature_row id="matrix_hovercraft"%}
<h3>The problem</h3>
<ul>
  <li>A lot of data is available on the Web, but in order to process & aggregate any piece of data, you need to manually develop the software for processing this specific data</li>
  <li>This is similar to how before the Web, you had to develop the code & infrastructure for connecting any 2 computers for allowing you to fetch some data from one computer to another</li>
  <li>The Web standardized this access model & made it easy to access any data around the world, but it didn't standardize the way to process this data</li>
</ul>
<h3>Solution overview</h3>
<ul>
  <li>The Web Wide Matrix doesn't treat data as just static information that is stored & exposed, but rather as something that needs to be continuously processed & manipulated to extract value from</li>
  <li>This is why it doesn't just model the data, but also the processing layer as part of the model</li>
  <li>The processing is done by software agents that live inside the Matrix buildings, & are hence called Residents, whose purpose is to process & organize the data - users tell them what they want, how they want the data to be organized & what value they want from it, & they continuously process the data to get the users what they want</li>
</ul>
<h3>The model</h3>
<ul>
  <li>The way the processing model is combined with the access model is using a layer inside the buildings that captures the processing state & value potential of buildings. We call it the "building smell", & its made available & propagated around buildings</li>
  <li>Residents move from building to building, attracted by their smell, & apply actions to process the data inside the buildings</li>
  <li>The seed knowledge of how to do this processing is provided using something called "Training courses", which are very easy to develop, & also available for download from vendors</li>
  <li>But beyond the seed knowledge, the Residents also learn thru feedback & exploration how to improve in processing data to satisfy users</li>
</ul>


## Interface model
An interface for effectively consuming information & data
{% include feature_row id="matrix_browser"%}

<h3>The problem</h3>
<ul>
  <li>The common abstraction of data is that of files & folders, data spreadsheets & letters</li>
  <li>The inherent problem with this abstraction is that all of these are based on reading pieces of data one by one</li>
  <li>This can only work if you have a very limited number of items
    <ul>
      <li>The metaphor we like for it is a baggage carousel in airports, that forces you to look at all items until you find what you want. This is only effective if you have few dozen items & not thousands.</li>
    </ul>
  </li>
  <li>The problem is that the amount of data we have today - user generated, device generated &c - is huge, & can't be effectively consumed in the current abstraction & interface</li>
</ul>
<h3>Solution overview</h3>
<ul>
  <li>The Web Wide Matrix doesn't just address the access & processing of information & data, but also how to effectively consume it</li>
  <li>In the real world we have 2 cognitive powers that we utilize all the time in order to perceive & find stuff out of thousands of items</li>
  <li>The 1st is something we call "Top-sight vision", & is the ability to look on a scene that contains thousand of items, & find what we're looking for in a few seconds
    <ul>
      <li>For example, if you are in a big department store, as long as you can see the different isles, you'll quickly see where the shoes or coats are</li>
    </ul>
  </li>
  <li>The 2nd is something we call "Spatial memory", which allows us to remember where we last saw something
    <ul>
      <li>For example, in your house you remember where you left something, or where the medicine or tools are</li>
    </ul>
  </li>
  <li>In order to leverage these 2 cognitive powers to consume large amounts of data & information, we need a different abstraction of data, which is more similar to the real-world.</li>
  <li>We call such type of interface an "Organized Space", & its basically a VR representation of data, allowing users to see all the data, quickly discover what they want, & also remember where they last saw something to find it or similar items again</li>
</ul>
<h3>The model</h3>
<ul>
  <li>In order to provide an organized space interface to its data, the rendering aspect of data is built-into the model</li>
  <li>Each building also have a visual 3D representation chosen to represent the data inside it</li>
  <li>When you look at the buildings within some floor, you get an overview of the data inside it</li>
  <li>Part of the work done by the Residents is to organize the data buildings within floors & rooms into an organized space, so that users can easily consume them, just like they easily discover & find stuff in supermarkets or stores, that also contain thousands of items</li>
  <li>The actual way users consume the data in the Web Wide Matrix is using a software tool called the Matrix Browser, which renders the organized spaces in VR interface, that will be available on many types of devices</li>
</ul>

<hr>

# Presentations

## The problem
Learn more on the underlying problem:
<script async class="speakerdeck-embed" data-id="6e7e73dea2c34fe9afd2b2f8da624a22" data-ratio="1.77777777777778" src="//speakerdeck.com/assets/embed.js"></script>

{% include youtube-link.html id="-lwkoSfXUGs" %}

<hr>
## The solution
Learn more on the Web Wide Matrix solution:
<script async class="speakerdeck-embed" data-id="8fdc1c3b76ba4dc181a986da0ca8bb38" data-ratio="1.77777777777778" src="//speakerdeck.com/assets/embed.js"></script>
{% include youtube-link.html id="mIIwTcQjuRU" %}


<hr>

# blog

* <a href="/blog/interview-with-udi">Interview with Udi (Sep 20, 2017)</a>
