# MagicFrame - FR/EN

Inspiré par ces deux projets / Inspired by these two projects :
- GammaTroniques (FR) : [GitHub](https://github.com/NoahJst/HomeAssistant-Config/blob/main/esphome/README.md) / [Youtube](https://www.youtube.com/watch?v=XyooZe_9hc0)
- Madalena (EN) : [GitHub](https://github.com/Madelena/esphome-weatherman-dashboard)

## Français

### Materiel

- [ESP32 + écran](https://www.amazon.fr/Waveshare-Electronic-Interface-Bluetooth-Raspberry/dp/B07MB7SVHQ)
- [Cadre RIBBA IKEA](https://www.amazon.fr/Ikea-Cadre-RIBBA-13-noir/dp/B0BW8SLP9C/ref=sr_1_4)
- [Impression 3D](https://www.thingiverse.com/thing:6427159) : vous pouvez en trouver d'autre en cherchant "waveshare", "esp32".

### Logiciels

- Home Assistant
- ESPHome
- Studio Code Server

### Installation

1. Connectez l'écran à l'ESP32, en vérifiant bien que les 2 petits interrupteurs "1" et "2" de l'ESP32 soient bien sur "A" et "ON". Dans le cas contraire, vous aurez des problèmes d'affichage sur l'écran.
2. À l'aide de Studio Code Server, dans votre dossier `/.config/esphome` (cf. image `Screenshot.png`) :
- copiez les fichiers `magicframe.yaml` et `secrets.yaml`
- ajoutez le contenu du dossier `/fonts` dans votre dossier `/fonts`
4. Toujours à l'aide de Studio Code Server, intégrez le contenu des fichiers `sensors.yaml` et `templates.yaml` dans vos fichiers YAML de configuration Home Assistant (cf. image `Screenshot.png`)
5. Mettez à jours les parties commentées des fichiers `magicframe.yaml`, `secrets.yaml` et `templates.yaml` avec vos propres informations (entity ID, identifiants, mots de passe, API key...)
6. Branchez l'ESP32 à votre ordinateur, lancez ESPHome et suivez les instructions pour installer `magicframe.yaml` sur votre ESP32.
7. Enjoy!

### Fonctionnalités

#### Mise à jour automatique de l'écran
Réglé pour une mise à jour toutes les 4h.

#### Prévision météo
Utilisation de l'intégration [Meteorologisk institutt (Met.no)](https://www.home-assistant.io/integrations/met).
Il faudra paramétrer votre ville et récupérer l'ID d'entité `weather.forecast_VotreVille` pour l'intégrer au fichier `templates.yaml`.
La prévision et la température principales sont celles au moment de la mise à jour de l'écran.
En-dessous, on a la prévision et les températures min. et max, pour la journée en cours et les 4 jours suivants.

#### Température et humidité de la maison
Utilisation de l'intégration [Tado°](https://www.home-assistant.io/integrations/tado), car j'ai des têtes thermostatiques de cette marque sur mes radiateurs.

## English

### Hardware

- [e-Paper ESP32 Driver Board](https://www.amazon.com/gp/product/B07M5CNP3B)
- [Waveshare 7.5inch E-Ink Display](https://www.amazon.com/waveshare-7-5inch-HAT-Raspberry-Consumption/dp/B075R4QY3L)
- [IKEA RIBBA Picture Frame](https://www.amazon.com/Ikea-Ribba-Picture-Frame-White/dp/B01JEFG1B8)
- [3D print](https://www.thingiverse.com/thing:6427159): you can find more by searching for "waveshare", "esp32".

### Software

- Home Assistant
- ESPHome
- Studio Code Server

### Installation

1. Connect the screen to the ESP32, making sure that the 2 small switches "1" and "2" on the ESP32 are on "A" and "ON". Otherwise, you will have display problems on the screen.
2. Using Studio Code Server, in your folder `/.config/esphome` (cf. picture `Screenshot.png`):
- copy the files `magicframe.yaml` et `secrets.yaml`
- add the contents of the folder `/fonts` in your folder `/fonts`
4. Still using Studio Code Server, integrate the contents of the files `sensors.yaml` et `templates.yaml`in your Home Assistant configuration YAML files (cf. picture `Screenshot.png`)
5. Update the commented parts of the files `magicframe.yaml`, `secrets.yaml` and `templates.yaml` with your own information (entity ID, identifiers, passwords, API key...)
6. Connect the ESP32 to your computer, launch ESPHome and follow the instructions to install `magicframe.yaml` on your ESP32.
7. Enjoy!

### Features
