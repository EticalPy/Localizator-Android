<p align="center"><a href="https://ibb.co/W0GpSQm"><img src="https://i.ibb.co/NrtnwXc/68747470733a2f2f692e696d6775722e636f6d2f444970754e54492e6a7067.png" alt="68747470733a2f2f692e696d6775722e636f6d2f444970754e54492e6a7067" border="0"></a></p>

<p align="center">
    <a href="https://twitter.com/AmbronoBogdan">
      <img src="https://img.shields.io/badge/-TWITTER-black?logo=twitter&style=for-the-badge">
    </a>
    &nbsp;
</p>


Conceptul din spatele lui Localizator Android este simplu: o pagină falsă care solicita locația. 

* Longitudine
* Latitudine
* Precizie
* Altitudine - Nu este întotdeauna disponibilă
* Direcția - Disponibilă numai dacă utilizatorul se deplasează
* Viteza - Disponibilă numai dacă utilizatorul se deplasează

Împreună cu informațiile despre locație, obținem și **Informații despre dispozitiv** fără permisiuni :

* ID unic folosind Canvas Fingerprinting
* Modelul dispozitivului - Nu este întotdeauna disponibil
* Sistem de operare
* Platformă
* Numărul de nuclee CPU - Rezultate aproximative
* Cantitatea de memorie RAM - rezultate aproximative
* Rezoluția ecranului
* Informații despre GPU
* Numele și versiunea browserului
* Adresa IP publică
* Adresa IP locală
* Port local


**Recunoașterea automată a adresei IP** se efectuează după primirea informațiilor de mai sus.

**Acest instrument este destinat exclusiv scopurilor educaționale, Localizator Android arată ce date poate colecta o pagina web malitioasa și de ce nu trebui să dați clic pe linkuri aleatorii și să acordați permisiuni critice, cum ar fi locația etc.**.

## Care este diferența față de IP GeoLocation

* Alte instrumente și servicii oferă o geolocalizarea IP,  deloc exactă și nu oferă locația țintei, ci locația aproximativă a ISP-ului.

* Localizator Android utilizează HTML API și obține permisiunea de localizare, apoi preia longitudinea și latitudinea folosind hardware-ul GPS care este prezent în dispozitiv, astfel încât Localizator Android funcționează cel mai bine cu telefoanele inteligente; dacă hardware-ul GPS nu este prezent, cum ar fi pe un laptop, Localizator Android revine la geolocalizarea IP sau va căuta coordonate în cache.  

* În general, dacă un utilizator acceptă permisiunea de localizare, precizia informațiilor primite este **de aproximativ 30 de metri**.

* Precizia depinde de mai mulți factori pe care îi puteți controla sau nu, cum ar fi :
  * Dispozitiv - Nu va funcționa pe laptopuri sau telefoane care au GPS-ul stricat.
  * Browser - Unele browsere blochează javascripts
  * Calibrarea GPS - Dacă GPS-ul nu este calibrat, puteți obține rezultate inexacte, iar acest lucru este frecvent.


## Șabloane

Șabloane disponibile : 

* NearYou
* Google Drive (sugerat de @Akaal_no_one)
* WhatsApp (sugerat de @Dazmed707)
* Telegram
* Zoom (Propus de @a7maadf)
* Google reCAPTCHA (Realizat de @MrEgyptian)

## Testat pe :

* Kali Linux
* BlackArch Linux
* Ubuntu
* Kali Nethunter
* Termux
* Parrot OS
* OSX - Monterey v.12.0.1

## Instalare

```bash
git clone https://github.com/EticalPy/Localizator-Android.git
cd Localizator-Android/
chmod +x install.sh
./install.sh
```


In order to run in tunnel mode, install ngrok by running this command in the terminal:
```bash
brew install ngrok/ngrok/ngrok

ngrok http 8080
````

## Usage

```bash
python3 localizator.py -h

utilizare: localizator.py [-h] [-k KML] [-p PORT] [-u] [-v]

opțiuni:
  -h, --help afișează acest mesaj de ajutor și iese din joc
  -k KML, --kml KML Nume fișier KML KML
  -p PORT, --port PORT Port server web [ implicit : 8080 ]
  -u, --update Verifică dacă există actualizări
  -v, --version Imprimă versiunea

##################
# Exemple de utilizare #
##################

# Pasul 1 : În primul terminal
$ python3 localizator.py


# Pasul 2 : În al doilea terminal, porniți un serviciu de tunel, cum ar fi ngrok sau nokey
ssh -R 80:localhost:8080 nokey@localhost.run
```

## Demo

**YouTube**


