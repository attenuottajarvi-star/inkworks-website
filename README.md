# InkWorks website

Kolme staattista sivua: etusivu (`index.html`), tuki (`support.html`) ja
tietosuojaseloste (`privacy.html`). Ei kääntäjää, ei riippuvuuksia — pelkkää
HTML/CSS, joten sivut toimivat sellaisenaan millä tahansa staattisella
hosting-palvelulla.

## Julkaisu GitHub Pagesilla (ilmainen)

**1. Kirjaudu GitHubiin VS Codessa**
Vasemmassa alakulmassa oleva tili-ikoni → "Sign in with GitHub" (tai
komentopaletista: "GitHub: Sign in"). Jos sinulla ei ole GitHub-tiliä, sen
luonti on ilmaista osoitteessa github.com.

**2. Julkaise tämä kansio GitHubiin**
Lähdehallinta-välilehdellä (Source Control) näkyy nappi "Publish to
GitHub" — valitse **Public**-repositorio (GitHub Pages ei toimi ilmaiseksi
yksityisellä repolla). Nimeä repo esim. `inkworks-website`.

**3. Ota GitHub Pages käyttöön**
Mene selaimessa juuri luotuun repoon → **Settings** → **Pages** (vasen
valikko). Kohtaan "Build and deployment" → Source: **Deploy from a
branch** → Branch: **main**, kansio **/ (root)** → Save.

**4. Yhdistä oma domain**
Samalla Pages-sivulla kohtaan "Custom domain" kirjoita `inkworksapp.com` ja
tallenna. (Repossa on jo valmis `CNAME`-tiedosto tätä varten, joten GitHub
tunnistaa domainin automaattisesti.)

**5. Osoita domain GitHubiin (DNS-tietueet)**
Mene sinne mistä ostit inkworksapp.com-domainin (domain-rekisteröijän DNS-
asetuksiin) ja lisää:

- Neljä **A-tietuetta** juuridomainille (`inkworksapp.com`), osoittamaan:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- Valinnainen **CNAME-tietue** `www`-aliakselle → `<github-käyttäjänimesi>.github.io`

DNS-muutosten leviäminen voi kestää muutamasta minuutista pariin tuntiin.

**6. Ota HTTPS pakolliseksi**
Kun domain on tunnistettu (Pages-sivulla näkyy vihreä merkki DNS:n
kohdalla), ruksi "Enforce HTTPS" samalta sivulta.

Sen jälkeen sivusto on osoitteessa `https://inkworksapp.com`, ja jatkossa
sivujen päivitys tarkoittaa vain tiedostojen muokkausta ja uutta pushia —
GitHub Pages julkaisee muutokset automaattisesti.
