# Oppimispäiväkirja: Hajautettu git

_Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?_

Osion perustehtävät, kuten haarojen luominen ja yhdistämispyyntöjen (Pull Request) tekeminen GitHubin web-käyttöliittymässä, olivat melko suoraviivaisia ja selkeitä.

Haastavinta oli yhdistämisristiriitojen (merge conflict) ja etämuutosten yhteensovittaminen paikallisen työtilan kanssa. Erityistä päänvaivaa aiheutti merkistökoodausongelma (UTF-16 vs. UTF-8) CSS-tiedostossa, joka sai koodin näyttämään sekavalta ja esti selaimen sekä Gitin normaalia toimintaa.

Ongelmat ratkesivat tutkimalla Gitin tilaa tarkasti (`git status`, `git log -p`), varmistamalla tiedostojen oikea koodausmuoto editorissa sekä hakemalla etärepositorion muutokset (`git pull` / `git fetch`) ennen paikallista yhdistämistä. GitHub Actions -työnkulkujen lokit auttoivat myös varmistamaan, että vaaditut vaiheet menivät läpi.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| ------- | ------ |
| `git switch -c <haara>` | Luo uuden haaran ja siirtyy siihen välittömästi. |
| `git switch <haara>` | Vaihtaa olemassa olevaan haaraan. |
| `git fetch` | Hakee etärepositorion uusimmat viitteet ja tiedot lataamatta niitä suoraan työtilaan. |
| `git pull` | Hakee ja yhdistää etärepositorion muutokset suoraan aktiiviseen paikalliseen haaraan. |
| `git push -u origin <haara>` | Vie paikallisen haaran GitHubiin ja asettaa etäseurannan. |
| `git merge <haara>` | Yhdistää määritellyn haaran muutokset nykyiseen haaraan. |
| `git branch -a` | Listaa kaikki paikalliset ja etärepositorion haarat. |
| `git branch -d <haara>` | Poistaa jo yhdistetyn paikallisen haaran. |
| `git tag <nimi>` | Luo pysyvän versionhallintatunnisteen aktiiviseen talletukseen. |
| `git stash` | Laittaa paikalliset tallentamattomat muutokset väliaikaisesti sivuun. |