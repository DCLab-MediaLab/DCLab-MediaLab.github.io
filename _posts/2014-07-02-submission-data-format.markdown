---
layout: post
title:  "Webdata data structure"
date:   2014-06-20 7:00
categories: data structure
---

##Beadando formatumok

- a reszletes task leiras és a RunSubmission2014 alapjan
(Meg frissitve lesz, a training data kiadasakor. Vagy email kuldenek...)

I. A futasoknal elvart fajlnev formatumok.

me14xx_YYY_ZZZ.EXT

A ZZZ helyen a futas nevet kell megadni (aminek informativnak kell lennie, de rovidnek).
Az YYY helyen legyen a csapat roviditett neve.
Az xx a feladatunkat jelenti, azaz a Search and Hyperlinking. (sh)
Az EXT a kiterjesztes, amit szinten a task hataroz meg. (pl. .txt, .xml)

A további konvenciok, amik task specifikusak:

Jeleznunk kell, melyik sub task-ot futasa (S - Search, L -Linking)
valamint azt, hogy mely informaciot vettük figyelembe a futaskor (Shot - jelenet...)
milyen metaadatra támaszkodott...

Talan a pelda jobban ertheto: me13sh_DCU_L_Sh_I_A_Lucene
me13sh - (tavalyi) Search and Hyperlinking feladat
DCU - a csapat roviditese
L - Linking
Sh- jelenet informaciok alapjan
I - LIMSI/Vocapia atiratokkal
A többire egyertelmu utalást nem találtam, de remelhetoleg ezen roviditesekrol meg adnak ki informaciot.
De erre következtetek:
A- vizsgált horgonyok alapjan
Lucene - Lucene-t hasznalva

1.) Search sub task
A keresesekre eredmenyul adott szegmensek kulon sorba keruljenek és mindegyik tartalmazza a kovetkezo mezoket
(ilyen sorrendben és whitespace-szel elvalasztva):
queryId Q0 fileName startTime endTime jumpingPoint rank confidenceScore runName

A mezok ertelmezese:
queryId-a kereses azonositoja
Q0-ez egy orokolt állandó
fileName- a videot azonositja, ahol a szegmens van
startTime-a video kezdo ideje
endTime- a video vege
jumpingPoint-ahol a felhasznalo kezdheti nezni a szegmenst (ha ez megegyezik a startTime-mal, akkor, copy)
rank- a video szegmens pozizioja az eredmeny listaban
confidenceScore- lebegopontos szám, ami jellemzi a rendszer megbizhatosagat, hogy a talalat az egy ismert elem-e
runName-a rendszer neve, ami futattaja a keresest (pl mi alapjen dolgozik... tobb kereses eseten)

2.) Linking sub task

anchorId Q0 fileName startTime endTime rank confidenceScore runName

3.) Anchor detection

Meg nem talaltam pontos informaciot.