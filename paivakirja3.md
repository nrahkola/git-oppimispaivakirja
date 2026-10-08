# Oppimispäiväkirja: Git projektissa

_Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?_

Yksin kehittäessä versionhallinta toimii turvaverkkona ja automaattisena varmuuskopiona. Se antaa vapauden kokeilla uusia ideoita omissa ominaisuushaaroissaan ilman pelkoa toimivan koodin hajoamisesta. Lisäksi selkeä commit-historia toimii muistiinpanoina: jos jokin lakkaa toimimasta, aiempien tallennuspisteiden vertailu ja tarvittaessa palauttaminen on vaivatonta.

_Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?_

Tiimityössä versionhallinta estää kehittäjiä ylikirjoittamasta toistensa työtä. Ominaisuushaarat mahdollistavat samanaikaisen rinnakkaisen kehityksen, ja yhdistämispyynnöt (Pull Request) tarjoavat luontevan paikan koodikatselmoinnille, laadunvarmistukselle ja keskustelulle ennen koodin viemistä päähaaraan. Se luo läpinäkyvyyttä: kuka tahansa tiimistä näkee, kuka teki muutoksen, milloin ja miksi.

_Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan._

Käyttäisimme GitHub Flow -mallia:

1. **Päähaara (`main` / `master`) pidetään aina toimintakuntoisena.** Kukaan ei puske sinne suoraan koodia.
2. **Jokaiselle tehtävälle tai toiminnallisuudelle luodaan oma haara** (esim. `feature/kirjautuminen` tai `fix/tyylit`) päähaarasta.
3. **Päivitä haaraasi säännöllisesti** hakemalla päähaaran muutokset (`git pull origin main`), jotta suuret yhdistämisristiriidat vältetään ajoissa.
4. **Kun työ on valmis, avaa Pull Request (PR)** GitHubissa päähaaraa kohti.
5. **Koodikatselmointi:** Vähintään yhden tiimiläisen tulee katselmoida ja hyväksyä PR ennen yhdistämistä.
6. **Yhdistäminen (Merge) ja siivous:** PR yhdistetään ja väliaikainen ominaisuushaara poistetaan sekä GitHubista että paikallisesti.

_Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?_

Opintojakso oli erittäin käytännönläheinen ja hyödyllinen. Konkreettiset terminaalikomennot, automaattitestaus GitHub Actionsilla ja todellisten merge-ristiriitojen ratkominen toivat hyvää rutiinia. Työmäärä oli sopiva ja tehtävät etenivät loogisesti. Jatkossa olisi mielenkiintoista nähdä vielä hieman enemmän esimerkkejä monimutkaisemmista Git-tilanteista, kuten rebase-komennon käytöstä ja interaktiivisesta historiasta.