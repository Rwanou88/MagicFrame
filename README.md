# MagicFrame - FR/EN

<p align="center">
<img src="https://github.com/user-attachments/assets/a6f44f41-5818-4442-afc4-017f5addda86" width="400"/>
<img src="https://github.com/user-attachments/assets/b979119b-fafe-4016-985f-2d873fd0a38e" width="400"/>
</p>

FR - Inspiré par ces projets

EN - Inspired by these projects

- GammaTroniques (FR) : [GitHub](https://github.com/NoahJst/HomeAssistant-Config/blob/main/esphome/README.md) / [Youtube](https://www.youtube.com/watch?v=XyooZe_9hc0)
- Madalena (EN) : [GitHub](https://github.com/Madelena/esphome-weatherman-dashboard)
- Tech Dregs (EN) : [Youtube](https://www.youtube.com/watch?v=qJuF58CjwIA)

## Materiel - Hardware
Amazon FR
- [ESP32 + écran](https://www.amazon.fr/Waveshare-Electronic-Interface-Bluetooth-Raspberry/dp/B07MB7SVHQ)
- [Cadre RIBBA IKEA](https://www.amazon.fr/Ikea-Cadre-RIBBA-13-noir/dp/B0BW8SLP9C/ref=sr_1_4)

Amazon US
- [e-Paper ESP32 Driver Board](https://www.amazon.com/gp/product/B07M5CNP3B)
- [Waveshare 7.5inch E-Ink Display](https://www.amazon.com/waveshare-7-5inch-HAT-Raspberry-Consumption/dp/B075R4QY3L)
- [IKEA RIBBA Picture Frame](https://www.amazon.com/Ikea-Ribba-Picture-Frame-White/dp/B01JEFG1B8)

3D printer
- [Thingiverse](https://www.thingiverse.com/thing:6427159)

FR- Vous pouvez en trouver d'autres en cherchant "waveshare", "esp32".

EN - You can find more by searching for "waveshare", "esp32".

## Logiciels - Software
- Home Assistant
  - [EN - Home Assistant : Installation](https://www.home-assistant.io/installation/)
  - [FR - Abrège : Fabriquer la box domotique parfaite !](https://www.youtube.com/watch?v=XyooZe_9hc0)
- ESPHome
  - [FR - Abrège : Tuto ESPHome 2022](https://youtu.be/3GbyYQHQvV8)
- Studio Code Server

## Installation - FR

1. Connectez l'écran à l'ESP32, en vérifiant bien que les 2 petits interrupteurs "1" et "2" de l'ESP32 soient bien sur "A" et "ON". Dans le cas contraire, vous aurez des problèmes d'affichage sur l'écran.
2. À l'aide de Studio Code Server, dans votre dossier `/.config/esphome` (cf. image [Screenshot.png](https://github.com/Rwanou88/MagicFrame/blob/d5d15970d22fd17562468809398384b56ce35467/pictures/Screenshot.png)) :
    - copiez les fichiers `magicframe.yaml` et `secrets.yaml`
    - ajoutez le contenu du dossier `/fonts` dans votre dossier `/fonts`
3. Toujours à l'aide de Studio Code Server, intégrez le contenu des fichiers `sensors.yaml` et `templates.yaml` dans vos fichiers YAML de configuration Home Assistant (cf. image [Screenshot.png](https://github.com/Rwanou88/MagicFrame/blob/d5d15970d22fd17562468809398384b56ce35467/pictures/Screenshot.png))
4. Mettez à jours les parties commentées des fichiers `magicframe.yaml`, `secrets.yaml` et `templates.yaml` avec vos propres informations (entity ID, identifiants, mots de passe, API key...)
5. Branchez l'ESP32 à votre ordinateur, lancez ESPHome et suivez les instructions pour installer `magicframe.yaml` sur votre ESP32.
6. Enjoy!

<p align="center">
<img src="https://github.com/user-attachments/assets/22bbd79e-67af-4a39-8ac2-9701a0a2f3db" width="400"/>
</p>

## Installation - EN
1. Connect the screen to the ESP32, making sure that the 2 small switches "1" and "2" on the ESP32 are on "A" and "ON". Otherwise, you will have display problems on the screen.
2. Using Studio Code Server, in your folder `/.config/esphome` (cf. picture [Screenshot.png](https://github.com/Rwanou88/MagicFrame/blob/d5d15970d22fd17562468809398384b56ce35467/pictures/Screenshot.png)):
    - copy the files `magicframe.yaml` and `secrets.yaml`
    - add the contents of the folder `/fonts` in your folder `/fonts`
3. Still using Studio Code Server, integrate the contents of the files `sensors.yaml` and `templates.yaml`in your Home Assistant configuration YAML files (cf. picture [Screenshot.png](https://github.com/Rwanou88/MagicFrame/blob/d5d15970d22fd17562468809398384b56ce35467/pictures/Screenshot.png))
4. Update the commented parts of the files `magicframe.yaml`, `secrets.yaml` and `templates.yaml` with your own information (entity ID, identifiers, passwords, API key...)
5. Connect the ESP32 to your computer, launch ESPHome and follow the instructions to install `magicframe.yaml` on your ESP32.
6. Enjoy!

## Fonctionnalités - Features

### * Mise à jour automatique de l'écran - Automatic screen update *

FR - Réglé pour une mise à jour toutes les 4h.
Le paramétrage est présent dans le fichier `magicframe.yaml`.

EN - Set to update every 4 hours.
The setting is present in the file `magicframe.yaml`.

### * Prévision météo - Weather forecast *
Integration : [Meteorologisk institutt (Met.no)](https://www.home-assistant.io/integrations/met).

FR - Utilisation de cette intégration.
Il faudra paramétrer votre ville et récupérer l'ID d'entité `weather.forecast_VotreVille` pour l'intégrer au fichier `templates.yaml`.
La prévision et la température principales sont celles au moment de la mise à jour de l'écran.
En-dessous, on a la prévision et les températures min. et max, pour la journée en cours et les 4 jours suivants.

EN - I'm using this integration.
You will need to set up your city and retrieve the entity ID `weather.forecast_YourCity` to integrate it into the file `templates.yaml`.
The main forecast and temperature are those at the time of the screen update.
Below, we have the forecast and the min. and max. temperatures, for the current day and the following 4 days.

<p align="center">
<img src="https://github.com/user-attachments/assets/05af2c0b-8508-4de5-b912-c87673f9b3d2" width="400"/>
</p>

### * Température et humidité de la maison - Home temperature and humidity *
Integration : [Tado°](https://www.home-assistant.io/integrations/tado)

FR - Utilisation de cette intégration car j'ai des têtes thermostatiques de cette marque sur mes radiateurs.
Les ID d'entité température et humidité sont à intégrer directement dans le fichier `magicframe.yaml`.
Il est possible d'afficher les infos de 5 pièces.

EN - I'm using this integration because I have thermostatic heads of this brand on my radiators.
The temperature and humidity entity IDs are to be integrated directly into the file `magicframe.yaml`.
It is possible to display information for 5 rooms.

<p align="center">
<img src="https://github.com/user-attachments/assets/df3f795d-aa0a-4c34-bb1e-b987ff0713d0" width="400"/>
</p>

### * Calendrier - Calendar *
Integration : [CalDAV](https://www.home-assistant.io/integrations/caldav)

FR - Utilisation de cette intégration pour récupérer l'agenda souhaité (iCloud).
L'ID d'entité est à intégrer dans le fichier `templates.yaml`.
Il est possible d'afficher les 5 prochains événements du calendrier (sur les 90 prochains jours).
Les emojis peuvent être pris en compte, il faudra les ajouter, au fur et à mesure des besoin, dans le fichier `magicframe.yaml`.

EN - I'm using this integration to retrieve the desired calendar (iCloud).
The entity ID is to be included in the file `templates.yaml`.
It is possible to display the next 5 calendar events (over the next 90 days).
Emojis can be taken into account, they will have to be added, as and when needed, in the file `magicframe.yaml`.

<p align="center">
<img src="https://github.com/user-attachments/assets/cec0014b-4b0b-4bde-a56d-cab2923c0b43" width="400"/>
</p>

### * Wifi invité - Guest Wifi *
ESPHome : [QR Code](https://esphome.io/components/qr_code.html).

FR - Utilisation du composant d'ESPHome.
Le paramétrage est présent dans le fichier `secrets.yaml`.

Voici comment est configuré le code QR : `WIFI:T:WPA;S:NomDeMonRéseau;P:MonMotDePasse;H:false;`
| Options   | Exemple         | Description                                                                     |
| :-------: | :-------:       | :-------                                                                        |
| T         | WPA             |  Type d’authentification : WEP, WPA ou aucun en cas d’absence de mot de passe.  |
| S         | NomDeMonRéseau	|  Nom de réseau SSID.                                                            |
| P         | MonMotDePasse   |  Mot de passe, à ignorer si « T » est vide.                                     |
| H         | true            |  "true" si le réseau SSID est caché (Facultatif)                                |

EN - I'm using the ESPHome component.
The setting is present in the file `secrets.yaml`.

This is how the QR code is configured : `WIFI:T:WPA;S:MyNetworkName;P:MyPassword;H:false;`
| Options   | Exemple         | Description                                             |
| :-------: | :-------:       | :-------                                                |
| T         | WPA             |  Authentication type: WEP, WPA or none if no password   |
| S         | MyNetworkName	  |  SSID Network Name                                      |
| P         | MyPassword      |  Password, ignore if "T" is empty                       |
| H         | true            |  "true" if the network SSID is hidden (Optional)        |

<p align="center">
<img src="https://github.com/user-attachments/assets/3e589afc-ce22-4e4c-9052-cb93871b2248" width="400"/>
</p>

### * Date et heure de mise à jour - Date and time of update *
FR - Affiche la date et l'heure de la dernière mise à jour de l'écran.

EN - Displays the date and time of the last screen update.

<p align="center">
<img src="https://github.com/user-attachments/assets/e047e738-e1e1-4497-93ff-19ff7939ead3" width="400"/>
</p>

## TO DO
FR - Traduire en français les dates des événements de l'agenda.

EN - Translate the dates of the calendar events into french.
