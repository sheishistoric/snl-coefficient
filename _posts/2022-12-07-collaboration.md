---
title: "Networking Comedy: SNL through Network Analysis"
date: 2022-12-07
author: Emily Esten
layout: post
summary: "How has SNL facilitated connections amongst community?"
---
One of the key aspects of our definition of an *SNL* film was that alumni worked on a project together. For me, that's one of the more interesting aspects of looking at *SNL* as a franchise. We can certainly talk about the box-office or *star* power *SNL*, but few of those successes are necessarily the result of *SNL* in the long-term. What makes Happy Madison Productions films *SNL* movies (at least by my line of thought) is not that Adam Sandler is involved, but that numerous *SNL* alumni - who met because of the show - continue to work together decades after their time in the cast. *30 Rock* has *SNL* DNA not just from Tina Fey's real-life experiences, but also because of the numerous cameos and casting decisions (not to mention the direct involvement of Lorne Michaels and Broadway Video.)

Looking at the alumni throughout the network, we start to see the importance of a few key alumni - particularly those of the early 2000s - play an important role in how we define "definitive *SNL*".

## Basic Network Analysis
Using Melanie Walsh's *Introduction to Cultural Analytics and Python*[^1], I created some quick networks visualizations to make sense of collaborations amongst *SNL* alumni. (These networks removes *Saturday Night Live* from the dataset, as that would connect everyone in the network.)

### Basic Network

In a network of potential *SNL* media (sans *SNL* itself), we see a high concentration of alumni in the center. Even zooming in, it's hard to distinguish individuals within the network - they all start to overlap. Those on the outskirts of this network - Nate Herman, Vanessa Middleton, Melanie Graham, James Eagan, Erik Marino, Allison Gates, Sarah Sherman, Molly Kearney, Aristotle Athari - are too new to the show to have developed significant projects outside it.

{% include collaboration/snl-network-wo-snl.html %}

In a network of definitive *SNL* media (sans *SNL*), the concentration changes only slightly. We still a strong concentration and overlap of individuals at the center, though alums start to appear on the outside of the network.

{% include collaboration/snl-network-wo-snl-definitive.html %}

## General Network Questions
### Who has the most number of connections in the network?
Connections in this case are represented by the lines in the network graphs. Each line represent a working relationship between two alumni - that they appeared in the same TV show, worked on a film together, or contributed to some project.  

#### Amongst potential SNL:
<div>
<table align="left">
  <tr><th align="center">SNL Alum</th><th align="center">Number of Connections</th></tr>
  <tr><td>Lorne Michaels</td><td>296</td></tr>
  <tr><td>Will Ferrell</td><td>294</td></tr>
  <tr><td>Amy Poehler</td><td>284</td></tr>
   <tr><td>Tina Fey</td><td>283</td></tr>
    <tr><td>Tim Meadows</td><td>283</td></tr>
    <tr><td>Martin Short</td><td>283</td></tr>
    <tr><td>Fred Armisen</td><td>280</td></tr>
    <tr><td>Rachel Dratch</td><td>278</td></tr>
    <tr><td>Bill Hader</td><td>278</td><</tr>
    <tr><td>Conan O'Brien</td><td>278</td></tr>
</table>
</div>

#### Amongst definitive SNL:
<div>
<table align="left">
  <tr><th align="center">SNL Alum</th><th align="center">Number of Connections</th></tr>
  <tr><td>Lorne Michaels</td><td>276</td></tr>
  <tr><td>Will Ferrell</td><td>243</td></tr>
  <tr><td>Tina Fey</td><td>235</td></tr>
   <tr><td>Jimmy Fallon</td><td>233</td></tr>
    <tr><td>Fred Armisen</td><td>231</td></tr>
    <tr><td>Amy Poehler</td><td>229</td></tr>
    <tr><td>Maya Rudolph</td><td>228</td></tr>
    <tr><td>Darrell Hammond</td><td>227</td></tr>
    <tr><td>Kenan Thompson</td><td>225</td><</tr>
    <tr><td>Bill Hader</td><td>223</td></tr>
</table>
</div>

### Who has the most number of connections in the network (if you factor in edge weight)?
Edge weight refers to the number of connections between two nodes. An edge in this network represents a working relationship between two alumni - the weight of the edge being multiple working relationships. For example, Tina Fey and Amy Poehler have worked together on a number of projects (strong edge weight) while Tina Fey and Bruce Handy have worked together of very few projects (weak edge weight.)

With this in mind, Will Ferrell appears to have a lot of connections across the network - not only does he have a lot of alumni connections throughout both networks, but he has numerous relationships with those alumni. (As we dive into the data further, it's less that Will Ferrell is performing alonside these individuals, but appears on many of the same types of media - *SNL*-related media, talk shows, producing credits, etc.) Tina Fey, Jimmy Fallon, Amy Poehler, and Adam Sandler also appear in both networks, further pointing to their importance as connectors with the *SNL* alumni community.   

#### Amongst potential SNL:
<div>
<table align="left">
  <tr><th align="center">SNL Alum</th><th align="center">Weighted Degree</th></tr>
  <tr><td>Will Ferrell</td><td>5820</td></tr>
  <tr><td>Tina Fey</td><td>5022</td></tr>
  <tr><td>Jimmy Fallon</td><td>4889</td></tr>
   <tr><td>Amy Poehler</td><td>4878</td></tr>
    <tr><td>Adam Sandler</td><td>4844</td></tr>
    <tr><td>Lorne Michaels</td><td>4689</td></tr>
    <tr><td>Fred Armisen</td><td>4430</td></tr>
    <tr><td>Chris Rock</td><td>4430</td></tr>
    <tr><td>Bill Hader</td><td>4405</td><</tr>
    <tr><td>Kevin Nealon</td><td>4258</td></tr>
</table>
<br />
  </div>

#### Amongst definitive SNL:

<div>
<table align="left">
  <tr><th align="center">SNL Alum</th><th align="center">Weighted Degree</th></tr>
  <tr><td>Lorne Michaels</td><td>3651</td></tr>
  <tr><td>Will Ferrell</td><td>2234</td></tr>
  <tr><td>Jimmy Fallon</td><td>2081</td></tr>
  <tr><td>Tina Fey</td><td>2041</td></tr>
   <tr><td>Amy Poehler</td><td>2023</td></tr>
    <tr><td>Fred Armisen</td><td>1845</td></tr>
    <tr><td>Adam Sandler</td><td>1811</td></tr>
    <tr><td>Seth Meyers</td><td>1805</td></tr>
    <tr><td>Dana Carvey</td><td>1771</td></tr>
    <tr><td>Maya Rudolph</td><td>1747</td><</tr>
</table>
<br />
  </div>

### Who connects the most other nodes in the network?

*Betweenness centrality* measures how frequently a node lies on short paths between other pairs of nodes.[^4] In this case, the higher the betweenness centrality for a given individual, the more connections that nodes makes to other nodes.

In both potential and definitive *SNL* media, Lorne Michaels reigns supreme within the network. As Kathrine mentions in her blog post on the feature films dominant in our study, Lorne is incredibly important to *SNL* alums for his connections and role as a producer. But more interesting here are how both lists diverge after Lorne. Older alumni feature more prominently amongst potential SNL media, but more recent alumni of the 2000s make the connections amongst recent relationships.

#### Amongst potential SNL:
<div>
<table align="left">
  <tr><th align="center">SNL Alum</th><th align="center">Betweenness</th></tr>
  <tr><td>Lorne Michaels</td><td>0.017263</td></tr>
  <tr><td>Conan O'Brien</td><td>0.013673</td></tr>
  <tr><td>Janeane Garofalo</td><td>0.012211</td></tr>
  <tr><td>Martin Short</td><td>0.010187</td></tr>
   <tr><td>Will Ferrell</td><td>0.00949</td></tr>
    <tr><td>Dennis Miller</td><td>0.009258</td></tr>
    <tr><td>Julia Sweeney</td><td>0.008873</td></tr>
    <tr><td>Bill Murray</td><td>0.008777</td></tr>
    <tr><td>Tim Meadows</td><td>0.008297</td></tr>
    <tr><td>Amy Poehler</td><td>0.008248</td><</tr>
</table>
<br />
  </div>

#### Amongst definitive SNL:
<div>
<table align="left">
  <tr><th align="center">SNL Alum</th><th align="center">Betweenness</th></tr>
  <tr><td>Lorne Michaels</td><td>0.064561</td></tr>
  <tr><td>Will Ferrell</td><td>0.013621</td></tr>
  <tr><td>Pete Davidson</td><td>0.012454</td></tr>
  <tr><td>Fred Armisen</td><td>0.010851</td></tr>
   <tr><td>James Downey (I)</td><td>0.010615</td></tr>
    <tr><td>Maya Rudolph</td><td>0.010289</td></tr>
    <tr><td>Kenan Thompson</td><td>0.009915</td></tr>
    <tr><td>Tina Fey</td><td>0.009603</td></tr>
    <tr><td>Bill Murray</td><td>0.009263</td></tr>
    <tr><td>Will Forte</td><td>0.009210</td><</tr>
</table>
  </div>
<br />

## References
[^1]: Melanie Walsh, Introduction to Cultural Analytics & Python, Version 1 (2021), https://doi.org/10.5281/zenodo.4411250.
