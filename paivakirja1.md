# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Peruskomennot (`add`, `commit`, `status`) olivat suoraviivaisia ja helppoja hahmottaa heti alusta alkaen. Hieman tarkkuutta vaati ymmärtää tiedoston elinkaari ja ero Gitin eri tilojen välillä: milloin tiedosto on *untracked*, milloin muokattu (*modified*), ja miten valmistelualue (*staging area*) toimii.

Erityisen opettavaista oli harjoitella muutosten perumista eri tasoilla:
- `git restore --staged` poistaa muutokset valmistelualueelta koskematta itse tiedoston sisältöön.
- `git restore` palauttaa seurannassa olevan tiedoston viimeisimmän commitin mukaiseksi, mutta ei vaikuta lainkaan seuraamattomiin (*untracked*) tiedostoihin. Niiden siivoamiseen tarvittiin `git clean -fd`.
- `git revert` kumoaa aiemman commitin turvallisesti luomalla uuden vastakkaisen talletuksen ilman historiatiedon katoamista.

Esteiden selvittämisessä auttoi erityisesti `git status` -komennon säännöllinen ajaminen jokaisen vaiheen jälkeen sekä Gitin omat vinkit ja selkeät virheilmoitukset.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| ------- | ------ |
| `git init` | Alustaa uuden paikallisen Git-repositorion nykyiseen hakemistoon |
| `git status` | Näyttää työtilan ja valmistelualueen tilan (seurannassa olevat, muuttuneet ja untracked-tiedostot) |
| `git add <tiedosto>` | Siirtää tiedoston tai muutokset työtilasta valmistelualueelle (staging area) seuraavaa tallennusta varten |
| `git commit -m "viesti"` | Tallettaa valmistelualueella olevat muutokset Git-historiaan annetulla viestillä |
| `git mv <vanha> <uusi>` | Nimeää tai siirtää tiedoston ja valmistelee muutoksen suoraan seuraavaan talletukseen |
| `git rm <tiedosto>` | Poistaa tiedoston työtilasta sekä Gitin seurannasta ja valmistelee poiston talletukseen |
| `git restore --staged <tiedosto>` | Poistaa tiedoston muutokset valmistelualueelta (unstage) muuttamatta tiedoston sisältöä työtilassa |
| `git restore <tiedosto>` | Palauttaa työtilassa muokatun tiedoston edellisen commitin mukaiseksi (hylkää tallentamattomat muutokset) |
| `git clean -fd` | Poistaa työtilasta kaikki seuraamattomat (untracked) tiedostot ja hakemistot |
| `git revert HEAD` | Kumoaa viimeisimmän commitin luomalla uuden talletuksen, joka tekee päinvastaiset muutokset historiaa pyyhkimättä |
| `git log` | Näyttää talletushistorian (commit-tunnisteet, tekijän, päivämäärän ja viestit) |
| `git log --stat` | Näyttää commit-historian lisäksi yhteenvedon muuttuneista tiedostoista ja muokattujen rivien määrästä |
| `git log --oneline` | Tiivistää talletushistorian yhteen riviin per commit |
| `git tag <nimi>` | Luo nimilapun eli tagin valittuun (tai aktiiviseen) commitiin version merkitsemiseksi |
| `git clone <osoite>` | Kloonaa etärepositorion paikalliselle koneelle |
| `git switch <haara>` | Vaihtaa aktiivista haaraa (esim. `paivakirja1`) |