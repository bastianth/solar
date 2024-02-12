# solar

:warning: Work-in-progress :warning:

This repository is about a solar installation and a combined DIY-battery at a German house. Goal of the hard- and software is to keep the feed-in to the public grid around zero, charge the battery by solar energy and use the stored energy if needed. 

The system is attached to the public grid - it is at this moment not capable of providing power during a blackout as it uses small grid inverters (they only work with a provided frequency on the AC-Side by the grid). 

## How it started ##

Small solar installations became quite popular in Germany in recent years. Due to the energy price hike after the war broke out in Ukraine electricity was priced near 0,40 € per kWh. To compensate, many households installed so called "balcony power plants" (direct translation from German). 

The installation of 2 solar panels and a microinverter could save a lot of money! In energy demanding households with installations like garden or pool pumps, electrical heating or cooling, IT servers, electric vehicles and so on nearly every produced kWh is used to feed the own demand. Therefore the return on invest (ROI) can be high. I've seen installations where the ROI can be hit after 4 years. It had a feed-in-rate of 5 %. 

If no battery is present it all depends on the consumption during the solar hours. If the house has a normal consumption rate and a solar installation of 600 W inverter power is installed a feed-in-rate around 30 - 50 % should be assumed. So the calculated ROI could double: It has to be multiplied by around 2 because the feed-in to the grid with a two-way meter is "free". Normal houses should get a ROI of around 8 to 10 years. This is still a quite good investment!

There is a fact that is even better than the money itself:
With this kind of small solar installation and good mounting conditions (roof, no shadows, free standing) we can assume to produce roughly 1 kWh per kWp per year. In this case we are generating 600 kWh of solar energy. Even if we feed them to the grid we reduce the carbon footprint of our electricity. One kWh of solar energy is marked with 35 gCO₂eq / kWh. Compared to the average electricity value of 400 gCO₂eq / kWh we save around 219 kg CO₂eq every year. 

(Data taken from https://app.electricitymaps.com/map and Germany, year 2023)

These small solar installations are quite simple to install and easy to get approved by the local grid operator. To ensure a full approved operation only 2 things are necessary:
  
- register the installation the responsible authority - Marktstammdatenregister

  https://www.marktstammdatenregister.de/MaStR/

- announce the installation to your distribution network operator

  searchlink in ressources, mostly done online or with pdf forms

## The meter ##

After the installation is done, the local grid operator checks your type of energy meter. If the meter is an older style with an aluminium rotor disc inside they will commission a change to a two-way electric meter. It is often done by third party companies that will contact the house owner some weeks after the announcment of the installation. The change of the meter is essential for the grid operator because the older style meters can spin backwards if the amount of energy produced is higher than needed. This is a good situation for the houseowner but an unwanted for the grid operator / energy provider. 
So they are quite fast for a reason!

You can find details about energy meters on https://en.wikipedia.org/wiki/Electricity_meter

Newer style meters often come with an optical interface. It can be read by IR diodes and some software. Exposed entities are for example:

- Total energy drawn
- Total energy feed-in
- Actual power
- Phase voltages
- Phase currents
- Current net frequency

To make the meter expose these and other entities it has to be unlocked by a PIN and a setting. To get the PIN just write a letter or e-Mail to your grid provider asking for the number. It will take a couple of weeks until they respond. Entering the PIN is done by a simple flashlight (a cellphone flashlight did not work as expected). 

Pre-build hardware can be found on eBay and Amazon. They are attached with a magnet that clips to the round interface socket on the meter. 

The software part on these devices is often done by *Tasmota Smart Meter Interface* - https://tasmota.github.io/docs/Smart-Meter-Interface/


## The panels ##

Text about the solar panels

## The battery ##

Building the energy storage, charging it with energy

## Wiring it all up ##

Wiring all the stuff together

## The controller ##

Controlling it via HomeAssistant



### Outstanding ressources ###

*in English*

- Tasmota documentation about SMI, with a vendor list of meters https://tasmota.github.io/docs/Smart-Meter-Interface/

*in German*

- use your address to search for your distribution network operator https://www.vnbdigital.de/
- possible solar yields for German cities https://photovoltaiksolarstrom.com/photovoltaiklexikon/solarertrag-staedte/
- to configure your Tasmota SMI https://hessburg.de/tasmota-wifi-smartmeter-konfigurieren/
