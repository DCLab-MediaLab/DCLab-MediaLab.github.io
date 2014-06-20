---
layout: post
title:  "Transcripts data structure"
date:   2014-06-20 12:00
categories: data structure
---



## LIUM Transcript

Ctm files made by LIUM with ASR technology

.ctm - This describes the time marked conversation input files to be used for scoring the output of speech recognizers via the NIST [sclite](http://www.itl.nist.gov/iad/mig/tests/sdr/1999/SRT_FAQ.html#SCLITE) program. Both the reference and hypothesis input files can share this format.
The ctm file format is a concatenation of time mark records for each word in each channel of a waveform. The records are separated with a newline. Each word token must have a waveform id, channel identifier which is always 1 for SDR, start time, duration, and word text.


LIUM transcript csv file fields:

(CTM :== FILENAME C BEGINTIME DURATION word  CONFIDENCE) where: 

* Filename - the given file's name with date & time of broadcast, bbc channel(1-4), title
* C - Always 1 for SDR ? no significance
* BeginTime - The begin time (seconds) of the word, measured from the start time of the file.
* Duration - The duration (seconds) of the word.
* Confidence - Optional confidence score. It is proposed that this score will be used in the future.

Example:

| Filename                         | C  | Beign Time | Duration | Word | Confidence |
| -------------------------------- |:--:|:----------:|:--------:|:----:|-----------:|
| 20080402_004500_bbcone_panorama  | 1  | 0.195	     | 0.02     | the  | 0.884      |
