# solar

This repository is about a solar installation and a combined DIY-battery at a German house. Goal of the hard- and software is to keep the feed-in to the public grid around zero, charge the battery by solar energy and use the stored energy if needed. 

The system is attached to the public grid - it is at this moment not capable of providing power during a blackout as it uses small grid inverters (they only work with a provided frequency on the AC-Side by the grid). 

## How it started ##

Small solar installations became quite popular in Germany in recent years. Due to the energy price hike after the starting war in Ukraine electricity was priced near 0,40 € per kWh. To compensate, many households installed so called "balcony power plants" - direct translation from German. 

These small solar installations are quite easy to install and easy to get approved by the local grid operator. To ensure a full approved operation only 2 things are necessary:
  
- register the installation to Marktstammdatenregister (online: https://www.marktstammdatenregister.de/MaStR/)
- announce the installation to your local grid operator  (mostly done online or due to pdf-files)

After this is done, the local grid operator checks your type of energy meter. If the meter is an older style with an aluminium rotor disc inside they will commission a change to a two-way electric meter. It is often done by third party companies that will contact the house owner some weeks after the announcment of the installation. The change of the meter is essential for the grid operator because the older style meters can spin backwards if the amount of energy produced is higher than needed. This is a good situation for the houseowner but a not-wanted situation for the grid operator / energy provider. 
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


The installation of 2 solar panels and a microinverter could save 

Outstanding ressources:

*in German*

- to configure your Tasmota SMI https://hessburg.de/tasmota-wifi-smartmeter-konfigurieren/
