---
layout: post
title:  "Data structure"
date:   2014-06-20 7:00
categories: data structure
---


## ProsodicFeatures

Prosodic features are features that appear when we put sounds together in connected speech.
Acronyms:
* ACF: Autocorrelation function
* ZCR: zero-crossing rate

ProsodicFeatures csv file fields:
* frameTime - frame time
* pcm_RMSenergy_sma - root-mean-square signal frame energy
* pcm_loudness_sma - the loudness as the normalised intensity raised to a power of 0.3
* voiceProb_sma - the voicing probability computed from the ACF
* F0_sma - The fundamental frequency computed from the Cepstrum.
* HNR_sma - log harmonics-to-noise ratio (HNR) computed from the ACF
* voiceQual_sma - output of fundamental frequency ‘quality’ (= ZCR of ACF)
* F0direction -  F0 direction (?)
* directionScore -  F0 direction score (?)

