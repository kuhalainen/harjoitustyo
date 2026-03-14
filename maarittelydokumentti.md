**Ohjelmointikieli:** Python

**Muut kielet joita osaan:**
- C++ (sen verran mitä Alon kurssissa tarvitsee)
- Haskell (Perusteet "Funktionaalinen Ohjelmointi 1" kurssin pohjalta)

**Mitä algoritmeja ja tietorakenteita toteutat työssäsi?**
- Trie tietorakenteella toteutettu markovin ketju.

**Minkä ongelman ratkaiset?**
- Uusien melodioiden generoiminen harjoitteludatasta löytyvien melodioiden perusteella. 

**Mitä syötteitä ohjelma saa ja miten niitä käytetään?**

Ohjelma saa yksinkertaisia monofoonisia melodioita (eli sellaisia, joissa soi yksi nuotti kerrallaan), ja niiden avulla muodostetaan trie tietorakenne, jonka avulla voidaan generoida uusia meloidoita. 

**Tavoitteena olevat aika- ja tilavaativuudet (esim. O-analyysit)**

Trie tietorakenteeseen sijoittaminen on aikavaatimukseltaan O(n), joten uskon trie tietorakenteen luomisen melodioiden perusteella onnistuvan lineaarisessa ajassa.
Veikkaan melodian generoimisen onnistuvan myös lineaarisessa ajassa, sillä se vaatisi vain sen, että käy tietorakenteen kerran läpi juuresta alkaen, ja valitsee jonkin haaran todennäköisyyksien perusteella.
Trie tietorakenteen tilavaativuus on 	parhaimmassa tapauksessa O(n) (kaikki melodiat ovat identtisiä), ja huonoimmassa tapauksessa O(wn) (kaikki melodiat olisivat toisistaan täysin erilaisia). Trie tietorakenteen hyötynä on se, että samalla tavalla alkaville melodioille voidaan uudelleenkäyttää samoja solmuja, jonka takia tilaa säästyy siihen verrattuna, jos datan tallentaisi vain esim. listoina. Koska musiikissa käytetty aakkosto on pieni, uskon tilavaativuuden olevan lähempänä O(n), mutta kuitenkin jossain huonoimman ja parhaimman tilanteen välillä.

**Lähteet, joita aiot käyttää.**

https://en.wikipedia.org/wiki/Markov_chain

https://en.wikipedia.org/wiki/Trie

Jonkinlainen sopiva datasetti melodioita, joita pystyy käyttämään generoimisessa. Näitä löytyy netistä paljon.

**Opinto-ohjelma**

Tietojenkäsittelytieteen kandidaatti (TKT) 

**Dokumentaatiokieli**

Dokumentaation teen englanniksi.

**Muita ideoita**

Tämän lisäksi haluaisin luoda sovellukseen mahdollisuuden tallentaa melodiat vital syntetisaattorin sallimaan .vital muotoon (vastaa .json tiedostoa) demoa varten. Tällöin melodiaa voitaisiin soittaa sekvenssinä syntetisaattorista. Ohjelma voisi myös jollain tavalla generoida tai randomoida muita syntetisaattorin parametrejä (esimerkiksi minkälainen ääni soittaa melodiaa, tai minkälaisia efektejä ääneen laitetaan), jolloin tuloksesta ja demosta saataisiin kiinnostavampi. En kuitenkaan koe tämän olevan reunaehto sovelluksen onnistumiselle (eli ei haittaa jos se ei onnistu), itse melodioiden generoiminen trie tietorakenteen perusteella olisi työn pääpointti ja ydin. Tämä olisi vain kiva lisä.
