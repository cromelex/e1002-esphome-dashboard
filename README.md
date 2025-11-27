# ReTerminal E1002 colour epaper - ESPHome powered Home Assistant Dashboard

## Contents:
This repository contains all the code and dashboard configurations used on my ReTerminal E1002 colour epaper display, running ESPHome and displaying dashboards from Home Assistant.

`esphome.yaml` contains the ESPHome code for the ReTerminal E1002. This code is based on ESPHome version 2025.11.X.
`hass-dashboard.yaml` contains the full raw dashboard used in Home Assistant.  
`e1002-automation.yaml` includes a sample automation to select the page to display + notify on low battery.  

`/images/wallpaper-sample.webp` is my own photo.  

## Requirements:
ESPHome minimum version is 2025.11.0, as this implemented the display `model` for the E1002.

The dashboard relies on the following custom cards, together with cardmod to optimise for the epaper display:  

custom:clock-weather-card  
custom:mushroom-template-card  
custom:bubble-card  
custom:calendar-card-pro  
custom:mushroom-chips-card  
custom:flower-card  

The wallpaper is just a picture card with a sample uploaded. On my personal setup I use [immich-kiosk](https://github.com/damongolding/immich-kiosk) to allow a single URL to display dynamic content from my Immich photo library.  

The ESPHome code requires running the [Puppet Addon](https://github.com/balloob/home-assistant-addons) version 2.4.0 or above to generate the screenshots and convert them to the right colours for the epaper to display.
Specifically, it relies on [pull request #25](https://github.com/balloob/home-assistant-addons/pull/25) and [pull request #37](https://github.com/balloob/home-assistant-addons/pull/37), as these implement the required functionality for dithering and display colour mapping. These were fully implemented in version 2.4.0.

## Photos of the dashboards:
Home page
![Home page](/images/home.webp?raw=true "Home page")

Wallpaper page
![Wallpaper](/images/wallpaper.webp?raw=true "Wallpaper Page")

Energy
![Energy page](/images/energy.webp?raw=true "Energy page")

Plants
![Plants page](/images/plants.webp?raw=true "Plants page")
