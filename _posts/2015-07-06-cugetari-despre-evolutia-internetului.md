---
layout: page
title: Cugetari despre evolutia internetului
date:  2015-07-06 12:00
author: Cristi Constantin
categories: personal
tags: ro
---

Aceasta este prima data cand scriu un articol atat de complex. Va rog sa fiti ingaduitori.

_Info: Acest articol foloseste multi termeni tehnici_.

Dupa parerea mea, **internet 1.0** a aparut in 1982, cand s-a inventat protocolul TCP/ IP.<br />
Apoi a aparut Gmail. Apoi MySpace, Facebook si Youtube.<br />
Faptul ca poti lasa comentarii unui produs pe eMag, poti scrie articole pe blog, poti incarca poze si filme, poti vedea stream-uri de stiri, asta inseamna **internet 2**.<br />
Internet 1 este static, in timp ce 2 este in continua evolutie.<br />
In prezent, pot spune ca suntem la internet 2.5.

**Internet 3.0** va fi personalizat 100% pentru fiecare consumator in parte, un prieten virtual care iti stie tabieturile, tine minte ce iti place si ce nu.<br />
Un asistent prietenos si inteligent.

Momentan sunt enorm de multe probleme cu serviciile pe care ni le ofera internetul:<br />
 - Nu exista un sistem unitar de identificare a utilizatorului. Exista logare prin Facebook, Google, Twitter si altele in lucru, dar nimic standard si complet;
 - Motoarele de cautare gen Google sau Bing nu inteleg cu adevarat cautarea, ele doar filtreaza niste cuvinte cheie intr-o baza de date. Se lucreaza si la asta, Google Now, Apple Siri, Microsoft Cortana si altele, dar mai e mult de lucru;
 - Este nesigur. Oricine poate "asculta teava" cum le place hackerilor sa spuna. Exista unele solutii, TLS/ SSL, dar nu sunt implementate peste tot si inca exista gauri de securitate. Si ca bonus, anumite organizatii pot sa te spioneze oricum, pentru ca informatia nu este securizata decat pe drumul dintre tine si server, nu este criptata pe server;
 - Este fragil. Printre exemple: in cazul unui net-split, nu mai poti accesa serverele din zona afectata. Exista DDOS, pentru ca exista servere centrale care pot pica. Este nevoie de load balancere, pentru directionarea traficului. Toate sunt hack-uri construite peste arhitectura curenta.
 - Este controlat, sau poate fi controlat de cateva persoane. Sunt cenzurate bloguri, poze, filme, din diferite motive. Internetul nu trebuie sa fie cenzurat, pentru ca este facut de oameni si pentru oameni.
 - Datele tale, nu iti apartin tie. Sunt suficiente cazuri in care s-a demonstrat ca ceea ce postezi pe retelele de socializare (vezi Facebook) nu iti apartine tie, ci companiei care detine reteaua de socializare. In cazul in care anumite autoritati decid ca vor sa iti vada profilul, sau sa iti citeasca toate mesajele private, reteaua de socializare le preda imediat. Iar angajatii Facebook pot vedea informatiile tuturor utilizatorilor, indiferent daca sunt private sau nu (nu mai gasesc sursa pentru informatia asta, dar are sens). Iar daca iti stergi informatiile, de fapt ele nu sunt sterse, ci doar ascunse.

Pentru unele din problemele de mai sus, exista Torrent, Freenet, Retroshare, Tahoe-LAFS, IpFS, Bitcoin si platforme gen Ethereum.<br />
Ele au un rol VITAL, pentru ca sunt puncte de plecare pentru ideile revolutionare. Abia incepem sa ne deschidem mintea pentru ceea ce ne pot oferi.

La fel cum ne-a luat (2006 - 1982 = 24) de ani sa inventam Twitter, va dura comparativ la fel de mult pana cand vom inventa acel "game changer" peste Torrent, sau Ethereum.

Si la final, ce lipseste cel mai mult, este un standard prin care serviciile sa comunice intre ele.<br />
Exista protocoale de comunicare low & middle level (Json RPC, XML RPC, SOAP), dar fiecare site in parte este izolat si trebuie accesat separat.

In prezent nu exista o metoda prin care de exemplu contul meu de Pinterest sa comunice total cu contul meu de Foursquare si mai departe cu Google Maps, astfel incat sa pot cauta dintr-un singur loc:

- _intrebarea 1_: vreau o lista de 3 localuri la care NU am mai fost, unde pot manca ceva bun! (raspuns personalizat)
- _intrebarea 2_: la care dintre ele, gasesc cea mai ieftina pizza? (raspuns contextual, pentru ca depinde de intrebarea precedenta)

Ca sa obtina informatiile astea, un dispozitiv trebuie sa stie: cine sunt, unde ma aflu, ce anume mi-ar placea sa mananc, ce am mai mancat in trecut,
dar cel mai important, unde anume se afla fiecare informatie si cum anume trebuie citite si interpretate datele, astfel incat sa rezulte ceva care sa aiba sens.<br />
Sunt chestii foarte complicat de implementat cu tehnologiile pe care le avem acum.

Solutia este un domeniu comun unde serviciile sa se poata inregistra si fiecare sa spuna ce stie sa faca, gen:

- Gmail: stie sa primeasca si sa scrie mail-uri;
- Maps: stie sa caute adrese pe harta si sa gaseasca localuri si cladiri;
- Pinterest: tine o lista cu lucruri care imi plac, inspiratie pentru desen, citate interesante, mancaruri favorite, etc, etc.

Din cate stiu, exista discutii pentru astfel de standard.

Si ca sa vorbesc si despre programare, cea mai tare chestie in ziua de azi este sa scrii cod care sa poata fi executat atat pe client, cat si pe server.<br />
Daca 75% din cod este partajat, rezulta productivitate 175%. Momentan doar Node.js poate face asta. (vezi isomorphic Javascript //isomorphic.net/)

Totusi, cine a dezvoltat la modul serios aplicatii in web, stie deja ca Javascript devine tot mai mult rezultatul final al unei compilari, nu un limbaj in care sa scrii direct. Pentru asta exista CoffeeScript, TypeScript by Microsoft, Dart by Google, etc.

Sunt in lucru standarde gen ES6, ES7 Harmony si mai departe, care vor aduce multe imbunatatiri, dar din pacate EcmaScript este greoi pentru cineva care nu lucreaza in domeniu, iar imbunatatirile nu fac decat sa adauge un strat de complexitate peste un limbaj deja prea complex.

O alta problema de productivitate este: de ce paginile web inca se mai scriu in HTML? In prezent, ca si in cazul Javascript, HTML este doar un "compile target".<br />
Si peste asta, HTML nici macar nu descrie continutul paginii, ci doar spune cum sa fie reprezentata.<br />
Exista taguri semantice gen ```<abbr>, <p>, <h1>```, dar majoritatea programatorilor nu le folosesc asa cum au fost gandite.

Imi aduc aminte, ca incepator, ce mult timp mi-a luat sa ma obisnuiesc cu sutele de paranteze ```<...> ... </...>``` din HTML...

Paginile ar trebui scrise in Slim, Jade, sau Haml, sau de ce nu Markdown sau Rst, ceva compact si prietenos. Prezentarea paginii conteaza enorm de mult!<br />
Din cauza asta CoffeeScript si Jade sunt atat de populare.

Sunt oameni cu foarte multe idei, dar cei cu idei nu au cunostinte suficiente cat sa le implementeze,
iar cei care stiu cum sa le implementeze, se pierd in implementare si nu au idei chiar atat de multe...

In secolul 21 lucrurile se misca ultra rapid, dar nu suficient de rapid...<br />
Pentru web, e nevoie de oameni care sa-si puna in aplicare singuri ideile, fara sa fie experti in programare.

Una dintre solutii ar fi ca limbaje gen **Python** sau **Ruby** sa fie integrate nativ in browsere.<br />
Amandoua limbajele sunt usor de invatat, prietenoase si productive, perfecte pentru incepatori. Exista comunitate si zeci de mii de librarii pentru ambele.

Pentru Python exista librarii experimentale gen Brython si Skulpt, care permit executarea de cod python in interiorul ```<script type="text/python">...</script>```.<br />
Sunt multe alte experimente gen FireBreath, sau IronPython in browser, fiecare cu o serie de dependinte, dar nimic nativ si complet portabil.

Sau, limbajul **Go**, nativ in browser. Atunci multe servicii distribuite gen ipFS si Ethereum s-ar integra nativ.

Acum ca a fost deschisa cutia Pandorei cu formatul binar pentru internet **Web Assembly**, browserele vor deveni framework-uri gigant, niste sisteme de operare in toata regula.

Estimez ca in urmatorii 5-10 ani, programatorii vor putea scrie cod nativ Python si Ruby pentru Chrome si Firefox.

Au mai fost incercari de formate binare: Java applet, Flash, Silverlight, dar toate au devenit irelevante. De ce?...

- Applet-urile Java sunt privite cu tot mai multa suspiciune din cauza nenumaratelor gauri de securitate descoperite in ultima vreme; Firefox te avertizeaza mereu cand pornesti applet-uri, iar Chrome le-a blocat complet, sa nu-si mai bata capul.<br />
- Flash, intr-o vreme se gasea in 80% dintre reclame... apoi a aparut Apple iOS, care a refuzat cu vehementa sa suporte flash (//www.apple.com/hotnews/thoughts-on-flash/). Apple vs Flash, Apple wins. Asta e povestea, really. Mai noi Adobe impinge puternic librarii de HTML5, vezi mai jos.<br />
- Silverlight nu este portabil. Punct. Proiectul "Moonlight" care trebuia sa porteze Silverlight nu mai este dezvoltat. Mai nou Microsoft impinge HTML5 masiv, de cand cu Windows 8++.

La nivel superficial, tot ce am zis mai sus e adevarat, dar in realitate, toate cele 3 au o singura problema: sunt niste produse care apartin unei companii.<br />
Si atunci e vorba de bani, compania decide in ce directie sa se miste produsul.

Daca as avea bani de investit intr-un limbaj de programare, in urmatorii 5 ani as investi in HTML5, care inseamna mai multe tehnologii, nu doar Javascript.

Si nu sunt singurul. Toate companiile relevante imping puternic HTML5. De ce? Pentru ca HTML5 nu apartine unei companii, ci este un standard general.

Hai sa vedem:

- Microsoft a inventat TypeScript (un limbaj care genereaza cod Javascript), Maker.js si are fork pe Node.js pe Github unde contribuie activ si intens.
- Google contribuie cu Angular, Polymer, Closure Compiler si multe altele.
- Facebook contribuie cu React, Flux, Immutable-Js, Jest, Regenerator, Nuclide si multe altele.
- Yahoo are Pure, Fluxible (un framework Flux), Atomizer, YUI si multe altele.
- Twitter are Bootstrap, Ratchet, Bower, Plumage.Js, Typeahead.Js, Hogan.Js si multe altele.
- Adobe are Snap.Js, Topcoat, Phonegap, Web fonts si Brackets (un editor HTML5!).
- Github contribuie cu Atom.io... si altele.

Toate sunt firme cu revenue de miliarde, sau sute de milioane de dolari.

Pe partea de browsere cred ca stam cel mai bine.

Microsoft a renuntat la **Internet Explorer** (care deja devenise o gluma) si il inlocuieste cu **Spartan/ Edge**, o parte din oamenii care au creat Opera dezvolta acum **Vivaldi** (in care eu imi pun toate sperantele), BitTorrent a lansat **Project Maelstrom** un browser pe baza de torrente, Tor a lansat **TorBrowser**, Ethereum lucreaza intens la **Mist**, iar Cyanogen isi fac propriul browser pentru Android.

Vor mai fi si altele.

Surse:

- https://en.wikipedia.org/wiki/History_of_the_Internet
- https://en.wikipedia.org/wiki/Gmail
- https://en.wikipedia.org/wiki/Myspace
- https://en.wikipedia.org/wiki/Facebook
- https://en.wikipedia.org/wiki/Twitter
- http://computer.howstuffworks.com/web-30.htm
- https://github.com/WebAssembly/
- https://github.com/jashkenas/coffeescript/wiki/List-of-languages-that-compile-to-JS/
- http://webdesign.about.com/od/htmltags/a/why-semantic-html.htm
