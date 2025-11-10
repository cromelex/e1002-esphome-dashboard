# ReTerminal E1002 colour epaper - ESPHome powered Home Assistant Dashboard

## Contents:
This repository contains all the code and dashboard configurations used on my ReTerminal E1002 colour epaper display, running ESPHOme and displaying dashboards from Home Assistant.

`esphome.yaml` contains the ESPHome code.
`hass-dashboard.yaml` contains the full raw dashboard used in Home Assistant.
`e1002-automation.yaml` includes the automation to select the page to display + notify on low battery.


## Requirements:
The dashboard relies on the following custom cards, together with cardmod to optimise for the epaper display:

custom:clock-weather-card
custom:mushroom-template-card
custom:bubble-card
custom:calendar-card-pro
custom:mushroom-chips-card
custom:flower-card

The wallpaper is just a picture card with a sample uploaded. On my personal setup I use [immich-kiosk](https://github.com/damongolding/immich-kiosk) to allow a single URL to display dynamic content from my Immich photo library.

The ESPHome codes requires running the [Puppet Addon](https://github.com/balloob/home-assistant-addons) to generate the screenshots and convert them to the right colours for the epaper to display.
Specifically, it relies on [pull request #30](https://github.com/balloob/home-assistant-addons/pull/30) as it implements the required functionality for dithering and display mapping.
