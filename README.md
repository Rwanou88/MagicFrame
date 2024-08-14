# MagicFrame - French

Inspiré par ces deux projets :
- GammaTroniques : [GitHub](https://github.com/NoahJst/HomeAssistant-Config/blob/main/esphome/README.md) / [Youtube](https://www.youtube.com/watch?v=XyooZe_9hc0)
- Madalena : [GitHub](https://github.com/Madelena/esphome-weatherman-dashboard)

## Materiel
- [ESP32 + écran](https://www.amazon.fr/Waveshare-Electronic-Interface-Bluetooth-Raspberry/dp/B07MB7SVHQ?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=epaper+esp32&sr=8-3&returnFromLogin=1&linkCode=sl1&tag=gammatronique-21&linkId=a08c0220b63548a858c0f70464056220&language=fr_FR&ref_=as_li_ss_tl)
- [Cadre IKEA](https://www.amazon.fr/Ikea-Cadre-RIBBA-13-noir/dp/B0BW8SLP9C/ref=sr_1_4?crid=DMCEA0VJL3D0&dib=eyJ2IjoiMSJ9.YcV2wYIdPlAein6ZE40bDa3ih_Ifb8dsHkJwdTfl0LDRTPSJMrI76W91slv28xFwfAAAENRYYCWqtbza_LjlRcLiyE0KOjPi-QjO0LTdv0B9giSHbgSfQFNdBEKOuUhXkuVATObGFpBlpu9iOKEUMOlbYsh2OQLkiNyVHsmyuM8kZeWSmOrLI_YjT8ZtDEPCpE-AcFzDGxl3tr_-licwEQaYkB3f5twewlcbFEehPWsMeUw_HuJhB5Rtu4S6bPfgJN3vWDa79N4qq0Eqv22GIw.OeI8xs3KO7CXwmHuujGfQe86ohRkRJQmVuiO3pCG9Ig&dib_tag=se&keywords=ikea+ribba&qid=1723619714&sprefix=Ikea+Ribba%2Caps%2C69&sr=8-4)

## Logiciel
- Home Assistant
- ESPHome

## Installation

1. No soldering is required since the e-Paper driver board was integrated into the ESP32 board. All I needed to do was to connect the e-Paper screen to the driver board, and then connect the driver board to the USB socket on my light switch.
2. Copy `/fonts`, `/images`, and `weatherman.yaml` to your /.config/esphome folder.
3. Integrate the content of `sensor.yaml` to your Home Assistant template configuration YAML file.
4. Install HA-GTFS-RT to your Home Assistant using HACS.
5. Once booted, flash `weatherman.yaml` the ESP32 board using ESPHome.
6. Enjoy!

# MagicFrame - English
