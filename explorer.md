---
layout: default
title: The SNL Coefficient Explorer
---

# The SNL Coefficient Explorer

Interact with the widgets on the left to query a subset of movies to plot.
Hover over the circles to see more information about each piece of media.

Based on Bokeh's [interactive query tool for a set of IMDB data](https://demo.bokeh.org/movies), which was in turn inspired by the [Shiny Movie Explorer](https://shiny.rstudio.com/gallery/movie-explorer.html).

<iframe src="https://snl-coefficient.herokuapp.com/main" title="SNL Coefficient Explorer" height="1000px" width="125%" zoom=".025"></iframe>

This project attempts to determine a value for cast and crew members' association with Saturday Night Live, to then determine how closely associated a particular media property is with the show. For the purposes of this project, cast and crew applies to 1) repertory players, 2) featured players, 3) staff writers, and 4) head writers, during the show's period.

Data for the **snl_cast_crew.csv** has been collected from Wikipedia, IMDB, and fan sources. More information can be found in this [Github repository](https://github.com/sheishistoric/snl_coefficient).