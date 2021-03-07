# AQUAS APP

Aquaponic monitoring and automation system based on NodeJs build on Arduino Enverionment

## Description
This system consists of a website interface and an Aquaponic kit

System Capabilities :

* Monitor water pH, water temprature, light intensity, and fish feed supply
* Automation of lighting and feeding
* Manual control of lighting, feeding, and pump
* Gmail notification

Aquaponic kit (Build on Arduino Environment)

![Aquaponic kit](https://user-images.githubusercontent.com/64517019/110229535-3692e680-7f45-11eb-8b96-afc3e3bf22a9.jpg width=250)

Website Interface (Based on NodeJs)

![Website Interface](https://user-images.githubusercontent.com/64517019/110229526-12cfa080-7f45-11eb-9f5c-acb96504886a.png width=250)

## Getting Started

### Hardware Requirement

hardawre requirement to build aquaponic kit

* ESP32
* 4 Channel Relay
* 12v Adaptor
* Ultrasonic Sensor
* Water Pump
* Ultrasonic Sensor (to monitor feed supply)
* BH1750 light intensity sensor
* E-201C water pH Sensor
* DS18B20 water temprature sensor
* servo motor to open fish feed container

### Software Requirement

* NodeJs
* MySQL
* MQTT Broker

### Instalation and Execution

* assamble the hardware according to the following block diagram 

![Block Diagram](https://user-images.githubusercontent.com/64517019/110229532-25e27080-7f45-11eb-8535-32c5d4c4fa65.png width=250)

* go to this link and follow the instruction to to make the database migration https://github.com/anandaPamungkas/aquas-seqelize-migration

* insert new administrator data to administrator table on your database manually

* provide an mqtt broker, you can use any mqtt hosting or you can also use a local mqtt broker

* make .env file using env-template that provided in this repo

* fill the .env file with your MySql Credential, MQTT broker credential, and gmail credential 

* change the websocket in main.js file according to your hosting if you're not using localhost

* run the application by executing "node bin/dev" command on your terminal

* login to admin dashboard using the credential that you entered previously in the administrator table

* for testing purposes you can also run aquas-kit-mimic script to replace the functionality of aquaponic kit by executing "node aquas-kit-mimic" 
