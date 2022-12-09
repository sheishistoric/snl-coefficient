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

Amongst potential SNL:
|-------------------------|----------------------|
| **SNL Alum**       | **Number of Connections** |
|--------------------|---------------------------|
| **Lorne Michaels** | 296                       |
| **Will Ferrell**   | 294                       |
| **Amy Poehler**    | 284                       |
| **Tina Fey**       | 283                       |
| **Tim Meadows**    | 283                       |
| **Martin Short**   | 283                       |
| **Fred Armisen**   | 280                       |
| **Rachel Dratch**  | 278                       |
| **Bill Hader**     | 278                       |
| **Conan O'Brien**  | 278                       |
|-------------------------|----------------------|


Amongst definitive SNL:
|-------------------------|----------------------------|
| **SNL Alum**            | **Number of Connections**  |
|-------------------------|----------------------------|
| **Lorne Michaels**       |276                        |
| **Will Ferrell**         |243                        |
| **Tina Fey**             |235                        |
| **Jimmy Fallon**         |233                        |
| **Fred Armisen**         |231                        |
| **Amy Poehler**          |229                        |
| **Maya Rudolph**         |228                        |
| **Darrell Hammond**      |227                        |
| **Kenan Thompson**       |225                        |
| **Bill Hader**           |223                        |
|-------------------------|----------------------------|


### Who has the most number of connections in the network (if you factor in edge weight)?
Edge weight refers to the number of connections between two nodes. An edge in this network represents a working relationship between two alumni - the weight of the edge being multiple working relationships. For example, Tina Fey and Amy Poehler have worked together on a number of projects (strong edge weight) while Tina Fey and Bruce Handy have worked together of very few projects (weak edge weight.)

With this in mind, Will Ferrell appears to have a lot of connections across the network - not only does he have a lot of alumni connections throughout both networks, but he has numerous relationships with those alumni. (As we dive into the data further, it's less that Will Ferrell is performing alonside these individuals, but appears on many of the same types of media - *SNL*-related media, talk shows, producing credits, etc.) Tina Fey, Jimmy Fallon, Amy Poehler, and Adam Sandler also appear in both networks, further pointing to their importance as connectors with the *SNL* alumni community.   

Amongst potential SNL:
|-------------------------|----------------------------|
| **SNL Alum**            | **Weighted Degree**        |
|-------------------------|----------------------------|
| **Will Ferrell**         |5820                       |
| **Tina Fey**             |5022                       |
| **Jimmy Fallon**         |4889                       |
| **Amy Poehler**          |4878                       |
| **Adam Sandler**         |4844                       |
| **Lorne Michaels**       |4689                       |
| **Fred Armisen**         |4430                       |
| **Chris Rock**           |4430                       |
| **Bill Hader**           |4405                       |
| **Kevin Nealon**         |4258                       |
|-------------------------|----------------------------|

Amongst definitive SNL:
|-------------------------|----------------------------|
| **SNL Alum**            | **Weighted Degree**        |
|-------------------------|----------------------------|
| **Lorne Michaels**       |3561                       |
| **Will Ferrell**         |2234                       |
| **Jimmy Fallon**         |2081                       |
| **Tina Fey**             |2041                       |
| **Amy Poehler**          |2023                       |
| **Fred Armisen**         |1845                       |
| **Adam Sandler**         |1811                       |
| **Seth Meyers**          |1805                       |
| **Dana Carvey**          |1771                       |
| **Maya Rudolph**         |1747                       |
|-------------------------|----------------------------|

### Who connects the most other nodes in the network?

*Betweenness centrality* measures how frequently a node lies on short paths between other pairs of nodes.[^4] In this case, the higher the betweenness centrality for a given individual, the more connections that nodes makes to other nodes.

In both potential and definitive *SNL* media, Lorne Michaels reigns supreme within the network. As Kathrine mentions in her blog post on the feature films dominant in our study, Lorne is incredibly important to *SNL* alums for his connections and role as a producer. But more interesting here are how both lists diverge after Lorne. Older alumni feature more prominently amongst potential SNL media, but more recent alumni of the 2000s make the connections amongst recent relationships.

Amongst potential SNL:
|-------------------------|---------------------------|
| **SNL Alum**            | **Betweenness**           |
|-------------------------|---------------------------|
| **Lorne Michaels**      |0.017263                   |
| **Conan O'Brien**       |0.013673                   |
| **Janeane Garofalo**    |0.012211                   |
| **Martin Short**        |0.010187                   |
| **Will Ferrell**        |0.00949                    |
| **Dennis Miller**       |0.009258                   |
| **Julia Sweeney**       |0.008873                   |
| **Bill Murray**         |0.008777                   |
| **Tim Meadows**         |0.008297                   |
| **Amy Poehler**         |0.008248                   |
|-------------------------|---------------------------|

Amongst definitive SNL:
|-------------------------|---------------------------|
| **SNL Alum**            | **Betweenness**           |
|-------------------------|---------------------------|
| **Lorne Michaels**      |0.064561                   |
| **Will Ferrell**        |0.013621                   |
| **Pete Davidson**       |0.012454                   |
| **Fred Armisen**        |0.010851                   |
| **James Downey (I)**    |0.010615                   |
| **Maya Rudolph**        |0.010289                   |
| **Kenan Thompson**      |0.009915                   |
| **Tina Fey**            |0.009603                   |
| **Bill Murray**         |0.009263                   |
| **Will Forte**          |0.009210                   |
|-------------------------|---------------------------|




## References
[^1]: Melanie Walsh, Introduction to Cultural Analytics & Python, Version 1 (2021), https://doi.org/10.5281/zenodo.4411250.
