Laddningstid och användbarhet
=======================

I den här uppgiften ska jag titta närmare på laddningstiden och responsiviteten hos tre olika webbsidor.

Urval
-----------------------

Jag har valt tre olika webbplatser av ungefär samma karaktär, för att de enklare ska kunna jämföras med varandra. De är: Försärkingskassan.se, folhälsomyndigheten.se, och skane.se (hemsidan för Region Skåne). Alla tre sidorna tillhör offentliga aktörer, och är relativt statiska och simpla i sitt innehåll. De får också antas ha som mål att vara så tillgängliga och användbara som möjligt.

Metod
-----------------------

All information lagras i ett Google-Kalkylark, som kan ses nedan. För varje webbplats körs tre olika sidor först genom Google Pagespeed-verktyget, både i mobil- och i desktop-version. Här antecknas betyget som verktyget ger till varje sida, och vilka förslag till förbättringar som beräknas ha störst effekt. Varje sida mäts sedan via network-filen i devtools. Där noterar jag sidans laddningstid, antalet resurser som laddas, samt sidans totala storlek. Varje sida mäts tre gånger, och snittet av resultaten antecknas. Möjliga förbättringar av varje webbplats diskuteras sedan.

Resultat
-----------------------

<h3>Data från undersökningen</h3>
<div class="spreadsheet-div">
<iframe class="spreadsheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQP8lH_8dVKKEwnoQVtbFqfdftCsoIGwuh-sTBRGxhTet38v8UyA5stLfQ2Hr4XDc3l4oLJwd8lpKht/pubhtml?widget=true&amp;headers=false"></iframe>
</div>

<h3>Försäkringskassan</h3>
<br>
![Snapshot från Försäkringskassan](%assets_url%/img/fk.png)
<br>
<br>

Försäkringskassans webbplats ligger i mitten när det gäller laddningstid, men har den överlägset största totala storleken. Detta får ses som imponerande. Samtidigt så har dock sidans mobilversion stora problem, och får väldigt låga betyg i Pagespeed. Problemet ligger framförallt i blockerande kod som måste köras innan sidan renderas, samt Javascript som laddas men som inte används. Samma problem påverkar desktop-versionen. Detta hade eventuellt kunnat lösas genom en bättre kodstruktur. På sök-sidan, där texten är mer omfattande, saktas sidan också ned av dåligt komprimerad text. 

<h3>Folkhälsomyndigheten</h3>
<br>
![Snapshot från Folkhälsomyndigheten](%assets_url%/img/fhm.png)
<br>
<br>

Folkhälsomyndighetens webbplats är mindre i sin totala storlek än Försäkringskassans, men tar ungefär lika lång tid att ladda. Den får dock betydligt bättre betyg i Pagespeed - det finns alltså färre möjligheter till förbättring. På mobilsidan finns dock en del förslag. Det gäller framförallt blockerande kod, dåligt komprimerad text, och i ett fall bilder som laddas i för stor storlek. Värt att notera är att antalet resurser är betydligt lägre här än hos Försäkringskassan. 

<h3>Region skåne</h3>
<br>
![Snapshot från Folkhälsomyndigheten](%assets_url%/img/skane.png)
<br>
<br>

Region Skånes hemsida får överlag de bästa betygen av Pagespeed, särskilt den mobila sidan. Samtidigt så tar den längst tid att ladda, men är bara i mitten när det gäller total storlek, samt i antalet resurser. Förslagen som ges gäller även här framförallt blockerande kod och oanvänd Javascript på de sidor som presterar sämst.

Analys
-----------------------
Av de tre sidorna får Försäkringskassans överlag det sämsta betyget av Pagespeed. Här finns stora möjligheter att göra sidan snabbare. Dock så är de främsta problemen ungefär de samma för all tre sidorna: Kodblock som måste utföras innan sidan laddas, samt Javascript som laddas men inte används. I andra hand så hade också bättre komprimerad text hjälpt, samt för vissa sidor ett bättre val av bildstorlekar.

Baserat på de mätningar som gjorts här känns det rimligast att ranka Folkhälsomyndighets hemsida högst. Den har visserligen inte allra högst betyg - det har Region Skåne. Men Region Skånes hemsida laddar en autospelande video, vilket eventuellt är förklaringen till att den tar betydligt längre tid att ladda än de andra sidorna. Videon känns onödig, och gör att sidan känns trögare. Folkhälsomyndighetens sida är å andra sidan snabb, har en låg total storlek och får genomgående goda betyg av Pagespeed - även om förbättringar finns att göra särskilt på mobil-sidan.

När jag prövar att ladda olika sidor så känns all laddningstid över en sekund som en märkbar fördröjning. Av de sidor som prövats här är det bara Region Skånes sida som inte klarar det kravet i genomsnitt - och den sidan är också den ändå som känns märkbart långsam. Samtidigt så har vissa sidor med mycket video- och bildinnehåll - som till exempel Youtube - en betydligt längre laddningstid. Eventuellt så uppfattar man det som mindre märkbart då det innehåll som laddas in är så stort, vilket gör att den längre laddningstiden känns rimlig.

Författare
-----------------------
Andreas Thiberg