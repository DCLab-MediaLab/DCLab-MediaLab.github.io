---
layout: post
title:  "Subtitle structure"
date:   2014-06-21 7:00
categories: data structure
---

The subtitle datastructure is basicly an xml, tha actual namespace is http://www.w3.org/2006/10/ttaf1, which stands for  Timed Text (TT) Authoring Format.

From the format only some tags are used, the structure looks like:

- tt
	- head : this is empty
	- body
		- div
			- (multiple) p : attribute 'begin' and 'end'
				- (one or multiple) span, br, etc

Below the "p" level, nothing is useful, so we want to strip everything, except the actual text.

Example: 

<p begin="00:00:06.433" end="00:00:09.785">
<span tts:color="#ffff00" tts:textAlign="center">
Louise, these last
<br/>
</span>
<span tts:color="#ffff00" tts:textAlign="center">few weeks have been really...</span>
</p>

Converted:

start time, end time, "text"
6.433, 9.785, "Louise, these last few weeks have been really..."