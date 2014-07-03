---
layout: post
title:  "Webdata data structure"
date:   2014-06-20 7:00
categories: data structure
---

##Beadand� form�tumok

- a r�szletes task le�r�s �s a RunSubmission2014 alapj�n
(M�g friss�tve lesz, a training data kiad�sakor. Vagy email k�ldenek...)

I. A fut�sokn�l elv�rt f�jln�v form�tumok.

me14xx_YYY_ZZZ.EXT

A ZZZ hely�n a fut�s nev�t kell megadni (aminek informat�vnak kell lennie, de r�vidnek).
Az YYY hely�n legyen a csapat r�v�d�tett neve.
Az xx a feladatunkat jelenti, azaz a Search and Hyperlinking. (sh)
Az EXT a kiterjeszt�s, amit szint�n a task hat�roz meg. (pl. .txt, .xml)

A tov�bbi konvenci�k, amik task specifikusak:

Jelezn�nk kell, melyik sub task-ot fut�sa (S - Search, L -Linking)
valamint azt, hogy mely inform�ci�t vett�k figyelembe a fut�skor (Shot - jelenet...)
milyen metaadatra t�maszkodott...

Tal�n a p�lda jobban �rthet�: me13sh_DCU_L_Sh_I_A_Lucene
me13sh - (tavalyi) Search and Hyperlinking feladat
DCU - a csapat r�vid�t�se
L - Linking
Sh- jelenet inform�ci�k alapj�n
I - LIMSI/Vocapia �tiratokkal
A t�bbire egy�rtelm� utal�st nem tal�ltam, de rem�lhet�leg ezen r�vid�t�sekr�l m�g adnak ki inform�ci�t.
De erre k�vetkeztetek:
A- vizsg�lt horgonyok alapj�n
Lucene - Lucene-t haszn�lva

1.) Search sub task
A keres�sekre eredm�ny�l adott szegmensek k�l�n sorba ker�ljenek �s mindegyik tartalmazza a k�vetkez� mez�ket
(ilyen sorrendben �s whitespace-szel elv�lasztva):
queryId Q0 fileName startTime endTime jumpingPoint rank confidenceScore runName

A mez�k �rtelmez�se:
queryId-a keres�s azonos�t�ja
Q0-ez egy �r�k�lt �lland�
fileName- a vide�t azonos�tja, ahol a szegmens van
startTime-a vide� kezd� ideje
endTime- a vide� v�ge
jumpingPoint-ahol a felhaszn�l� kezdheti n�zni a szegmenst (ha ez megegyezik a startTime-mal, akkor, copy)
rank- a video szegmens poz�zi�ja az eredm�ny list�ban
confidenceScore- lebeg�pontos sz�m, ami jellemzi a rendszer megb�zhat�s�g�t, hogy a tal�lat az egy ismert elem-e
runName-a rendszer neve, ami futattaja a keres�st (pl mi alapj�n dolgozik... t�bb keres�s eset�n)

2.) Linking sub task

anchorId Q0 fileName startTime endTime rank confidenceScore runName

3.) Anchor detection

M�g nem tal�ltam pontos inform�ci�t.