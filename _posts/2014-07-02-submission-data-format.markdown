---
layout: post
title:  "Webdata data structure"
date:   2014-06-20 7:00
categories: data structure
---

##Beadandó formátumok

- a részletes task leírás és a RunSubmission2014 alapján
(Még frissítve lesz, a training data kiadásakor. Vagy email küldenek...)

I. A futásoknál elvárt fájlnév formátumok.

me14xx_YYY_ZZZ.EXT

A ZZZ helyén a futás nevét kell megadni (aminek informatívnak kell lennie, de rövidnek).
Az YYY helyén legyen a csapat rövídített neve.
Az xx a feladatunkat jelenti, azaz a Search and Hyperlinking. (sh)
Az EXT a kiterjesztés, amit szintén a task határoz meg. (pl. .txt, .xml)

A további konvenciók, amik task specifikusak:

Jeleznünk kell, melyik sub task-ot futása (S - Search, L -Linking)
valamint azt, hogy mely információt vettük figyelembe a futáskor (Shot - jelenet...)
milyen metaadatra támaszkodott...

Talán a példa jobban érthetõ: me13sh_DCU_L_Sh_I_A_Lucene
me13sh - (tavalyi) Search and Hyperlinking feladat
DCU - a csapat rövidítése
L - Linking
Sh- jelenet információk alapján
I - LIMSI/Vocapia átiratokkal
A többire egyértelmû utalást nem találtam, de remélhetõleg ezen rövidítésekrõl még adnak ki információt.
De erre következtetek:
A- vizsgált horgonyok alapján
Lucene - Lucene-t használva

1.) Search sub task
A keresésekre eredményül adott szegmensek külön sorba kerüljenek és mindegyik tartalmazza a következõ mezõket
(ilyen sorrendben és whitespace-szel elválasztva):
queryId Q0 fileName startTime endTime jumpingPoint rank confidenceScore runName

A mezõk értelmezése:
queryId-a keresés azonosítója
Q0-ez egy örökölt állandó
fileName- a videót azonosítja, ahol a szegmens van
startTime-a videó kezdõ ideje
endTime- a videó vége
jumpingPoint-ahol a felhasználó kezdheti nézni a szegmenst (ha ez megegyezik a startTime-mal, akkor, copy)
rank- a video szegmens pozíziója az eredmény listában
confidenceScore- lebegõpontos szám, ami jellemzi a rendszer megbízhatóságát, hogy a találat az egy ismert elem-e
runName-a rendszer neve, ami futattaja a keresést (pl mi alapján dolgozik... több keresés esetén)

2.) Linking sub task

anchorId Q0 fileName startTime endTime rank confidenceScore runName

3.) Anchor detection

Még nem találtam pontos információt.