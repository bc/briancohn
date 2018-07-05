# Utilities
## Docker
`services start docker`
`docker images` and `docker ps -a` -a to show nonrunning containers too
`docker run --name="container-name" image-name`

```
docker stop container-name

then you can
docker rm container-name|container-ID

delete all docker containers that are exited:
docker rm $(docker ps -a -q -f status=exited) 

to remove a container:
docker rmi repo:id

once you get it working smoothly
docker push repo-name:tagname

You can restart an existing container after it exited and your changes are still there.

docker start  `docker ps -q -l` # restart it in the background
docker attach `docker ps -q -l` # reattach the terminal & stdin

I use:
docker start dev0
docker attach dev0
and if you want another terminal, 
docker exe -it dev0 bin/bash

```

## Human Logistics
[https://doodle.com/create][Doodle]
[http://whenisgood.net/][WhenIsGood]

## Cheat Sheets
[http://www.grymoire.com/Unix/Sed.html#uh-0][Sed tutorial for regx substitutions]
[https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet][Markdown Cheatsheet]
[https://www.tug.org/twg/mactex/tutorials/ltxprimer-1.0.pdf][Latex Extended Guide]
[https://reu.dimacs.rutgers.edu/Symbols.pdf][Latex Symbols & Equations]

## Evaluation Rubrics
[http://www-scf.usc.edu/~csci401/finalproject/FinalProjectPresentationGradingRubric.pdf][CSCI401 Capstone Presentation]

## ggplot2
[http://ggplot2.tidyverse.org/reference/ggtheme.html][ggthemes]
[https://web.archive.org/web/20160320034441/cran.r-project.org/web/packages/GGally/vignettes/ggpairs.html][ggpairs]
[https://github.com/ropensci/plotly][ggplotly]
[https://github.com/rstudio/cheatsheets/blob/master/data-visualization-2.1.pdf][PDF Cheat Sheet to ggplot2, by tidyverse]
## Bokeh
[http://holoviews.org/gallery/index.html][holoviews]
[http://www.ancienteco.com/2012/05/quickly-visualize-your-whole-dataset.html][Visualize tableplot of data]


# R tip
Warnings as errors: `options(warn=2)`   
`options(error=browser)` or default as `options(error=NULL)`

# Electronics
[https://www.youtube.com/watch?v=pTVek7v0_R8][NOT gate]

# iTerm/SublimeText
`bash /Users/briancohn/scripts/iterm_open_with.sh \5 \1 \2 `
[https://gist.github.com/trinitronx/f59a8308d42d71fdba41][Command click to subl to specific line]


# Linux Setup
[https://askubuntu.com/questions/160036/how-do-i-disable-acpi-when-booting][How to disable ACPI on bootup to allow MsI COMPATIBILITY]
[https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository][Set up Docker]
`sudo usermod -a -G docker $USER` To make docker accessible to the user without `sudo`
