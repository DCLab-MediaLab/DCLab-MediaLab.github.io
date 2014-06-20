---
layout: post
title:  "Webdata data structure"
date:   2014-06-20 7:00
categories: data structure
---

##Webdata

webdata/cast/*.txt

These .txt files include three kinds of data for each video segment. 
The data describe characters that appeared in the actual video.
There are as many lines as characters. 
In each line we can find three kinds of data that is separated by "|" character.

The structure is the following: 
       actor's first name|actor's family name|played character

Example: 
       Sharon|Horgan|Donna 

(If the actor has more than two names, the first column includes one and the other names belong to second column.)
