---
title: The Definitive SNL
date: 2022-11-01
author: Kathrine Esten
layout: post
summary: "Potential *SNL* Media spans many genres"
---

At the very heart of this project, we wanted to learn the genre distribution of potential *SNL* media.  

While comedy dominates the official *SNL* media output, we were curious as to the second most-frequent genre. Was it the late night talk shows dominated by alumni like Conan O'Brien and Jimmy Fallon? Or was it animated films like *Inside Out* (2015) and *Hotel Transylvania* (2012) that would take a surprising second?

Based on our data set, we generated a table of the most frequent genres used on IMDB:

{% include definitive_snl/definitive_snl_chart.html %}

As a note, many projects on IMDB are labeled as multiple genres. For example, *SNL* and several *"Best Of"* specials are categorized as "music" due to the live musical performances featured on the show.

## Key Findings
**"Documentary" is the second most-frequent genre for potential *SNL* media**

**Three categories had only one project apiece and all had Lorne Michaels as a co-producer**:
 - Western: *Three Amigos* (1986)
 - Sport: *Hot Rod* (2007)
 - Horror: *Vampires vs the Bronx* (2020)

**Only four "talk shows" had coefficients higher than 1**
 - *Late Night with Conan O'Brien* (1993)
 - *Late Night with Conan O'Brien: 5* (1998), an anniversary special
 - *The 66th Primetime Emmy Awards* (2014)
 - *The Howard Stern Birthday Bash* (2014)

## Analysis

With almost fifty years of history behind it, *SNL* and its alumni have spawned a great number of documentary pieces such as *Live From New York* (2015) and *Belushi* (2020). It is also of note that *"Best Of"* specials are counted as documentary by imbD categorization, further inflating this genre's representation on our graph. As a fun fact, the highest non-*SNL* related (ie. not produced by NBC or associated with the show) was 2018's *Love, Gilda*.

In the coversation of whether documentary-style pieces should qualify as *SNL* media, this evidence perhaps merits further clarification of what standards exist for *SNL* movies/media: are they fictional?

Examining the other key findings, it is clear that Lorne Michael's designated coefficient of 1 leads to a major boost for projects that he co-produces, particularly when they involve prominent alumni. *Hot Rod* and *Three Amigos* each have a coefficient over 3 (3.003 and 3.857, respectively) and *SNL* cast members as leads, but neither appears in a standard list of *SNL* films. *Three Amigos* is also unique among our data points as one of Michaels' few writing credits.

For talk shows, the coefficient is limited in its analysis: by measuring total amount of episodes, any impact *SNL* alumni have on the show is incredibly diluted.

Ultimately, the genre bar graph confirms that the *SNL* franchise and other potential *SNL* media are mostly comedy; most other genres are secondary or tertiary genre categories. *Baby Mama* (2008), for example, is both a "comedy" and a "romance."

{% include definitive_snl/definitive_snl_genres_bar_chart.html %}
