# Fire Control

Author: Eduardo Neville

Sciper: 314667

### Making Inteligent Things - Team Project Proposal

This project will be worked on in tandem with the Software Enterprise course where we will develop the app with which users will be able to interact with this projects output stream. To follow and see the full project check out our github on this [link](https://github.com/EduardoNeville/fire_patrol)

**Note:** Many of the components are subject of discusion so as to optimize the capabilities of the different devices to their full potential. They many or many not be updated as we continue doing research.

### Description of project

As climate change has more and more of an effect on our world, natural environments become drier - particularly in the mediteranean climate. This leads to fires being more and more dangerous every year. Whilst forest-fires are rare, it only takes one catastrophe to completely ravage an entire ecosystem. Early detection and action is therefore key to prevent them from becoming untamable. This is why we propose to build a network of sophisticated cameras that will monitor the eco-system to better help detect and prevent wild-fires.

In our system we envision a set of sentries all connected to a main observer that would monitor and detect potential fires and alert accordingly. This observer collects the data from each of the sentres thermal cameras and transfers the data to a database which then, be powered by a detecion machine learning model using Computer Vision, asseses the images and detects fires. Once detected using the sentries it pin points the location of the fire.

## Observer

The main observer will collect the data from the different sentries and transfer the data back to a database to detect fires in the area.

To obtain information from the different sentries the observer is connected to the other sentries via a wireless connection. Through it the sentries stream their recordings to the main observer how then processes them and sends them to a main datacenter.

This can be done through either a wireless network such as the one in this example:

[Link](https://www.youtube.com/watch?v=xb7psLhKTMA)

Or using a long range wireless comunication channel such as this one:

[Tutorial for long range wireless 1.8km](https://www.instructables.com/Long-Range-18km-Arduino-to-Arduino-Wireless-Commun/)

[Youtube tutorial for same component from recommended youtube channel](https://www.youtube.com/watch?v=vqRqtgvltOI)

### Components for the observer

| Components | Use case | Price (CHF) | URL |
| :---| :---: | :---: | ---: | 
| Arduino | Used to set up | 9 | [Link](https://www.banggood.com/Geekcreit-UNOR3-ATmega328P-Development-Board-No-Cable-Geekcreit-for-Arduino-products-that-work-with-official-Arduino-boards-p-964163.html?imageAb=2&akmClientCountry=ES&p=FA25224129409201603Q&akmClientCountry=ES&cur_warehouse=USA) |
| HC-12 Long Range | Wireless comunication| 9 | [Link](https://es.banggood.com/Geekcreit-HC-12-433MHz-SI4463-Wireless-Serial-Module-Wireless-Transceiver-Transmission-Serial-Communication-Data-Board-Remote-1000M-p-973522.html?imageAb=2&akmClientCountry=ES&p=FA25224129409201603Q&a=1709495282.6898&akmClientCountry=ES&cur_warehouse=CN)|

## Sentry

The main project will focus on creating a sentry that is able to send a video stream of different types to our data center. On top of that it must be able to be self suficient using solar panels to keep it's power supply.

**Note:** Further information must be found as to how the sentry will operate. eg: Will it have to rotate on itself to have a 360 view? Will it also have a secondary axis of rotation to account for slope degree.

### Components for a single sentry

These are the main components of the sentry (each link will take you to their section in the document)

| Components | Use case | Section |
| :---| :---: | ---: | 
| Arduino | MicroControllers for different purposes | [Link](#microcontrollers) |
| Thermal cameras | Fire detection unit | [Link](#thermal-cameras)|
| Regular camera | Distance and real view tracking | [Link](#regular-cameras) |
| Long range distance sensor | Location of fire in GPS | [Link](#) |
| Solar Panels | Keeps the sentry working | [Link](#solar-panels) |
| LithiumPolymer Batteries | Supply current cameras | [Link](#batteries) |

### [ 0 ] Microcontrollers

Choosing a micro controller depends on what sensors we will end up using as some require specific models.

Here are a few of the controllers we might needed

| Controller | Use case | Price (CHF) | URL |
| :---| :---: | :---: | ---: | 
| Arduino | Used to set up | 9 | [Link](https://www.banggood.com/Geekcreit-UNOR3-ATmega328P-Development-Board-No-Cable-Geekcreit-for-Arduino-products-that-work-with-official-Arduino-boards-p-964163.html?imageAb=2&akmClientCountry=ES&p=FA25224129409201603Q&akmClientCountry=ES&cur_warehouse=USA) |

### [ 1 ] Vision

This is the bread and butter of our project. Our cameras will have to capture during extended periods of time fires. This will be done using thermal cameras as well as regular cameras to tell where it's a fire or a bbq for example.

#### Thermal Cameras

Here is a link to an example build of a thermal camera. [Example Project](https://projecthub.arduino.cc/jdanielse/amg8833-thermal-camera-1dfb5a)

##### List of thermal cameras
| Name | Price (CHF) | URL |
| :---| :---: | ---: | 
| AMG8833 Thermal Camera | 21 | [Link](https://es.aliexpress.com/item/1005001991332288.html?spm=a2g0o.order_list.0.0.21ef180278wPcp&gatewayAdapt=glo2esp)|
| FLIR Radiometric Lepton Dev Kit V2 | 226 | [Link](https://www.sparkfun.com/products/15948)| 
| FLIR Lepton 2.5 - Thermal Imaging Module | 184.66 |[Link](https://www.sparkfun.com/products/16465) | 

Further information in these links:

[Link](https://forum.arduino.cc/t/temperature-measurement-at-long-distance-100-meters/59754) 

[Link](https://www.reddit.com/r/arduino/comments/5sja4p/need_help_choosing_a_long_range_ir_camera_for/)

[Link](https://forum.arduino.cc/t/esp32-camera-long-range-cctv/969079)

#### Regular Cameras

A regular camera could help us find the distance of objects withouth having to use a disntace sensor. It could also help identify a fire through visual contact and confirm the thermal imaging.

##### List of cameras

| Name | Price (CHF) | URL |
| :---| :---: | ---: | 
| Arducam 5MP Plus OV5642 Mini Camera Module | 37 | [Link](https://www.sparkfun.com/products/18440) | 
| BETAFPV C02 FPV Micro Camera | 16 | [Link](https://maxterdrone.com/es/camaras-fpv/1969-betafpv-c02-fpv-micro-camera.html) |

#### Long range distance sensor 

Used to pin point the location of the fire and triangulate it's geo-location

##### List of components
| Name | Price (CHF) | URL |
| :---| :---: | ---: | 
| 150m Long Range Distance Sensor Arduino | N/A | [Link](https://www.jrt-measure.com/2004-2021-new-laser-distance-sensor/57612570.html) |
| Long Range Precise Ultrasonic Sensor Module for Arduino | N/A |[Link](https://www.laserrangesensor.com/showroom/long-range-precise-ultrasonic-sensor-module-for-arduino.html) |

### [ 2 ] Power Supply

#### Solar Panels

Here is a link as to how we will be using and implementing a solar panel to power the system. [Example project](https://www.circuitbasics.com/how-to-use-solar-panels-to-power-the-arduino/)

List of components:

| Name | Price (CHF) | URL |
| :---| :---: | ---: | 
| TP4056 battery charge controller | 7-9 |[Link](https://www.amazon.es/s?k=MakerFocus+10pcs+TP4056+Charging+Module+with+Battery+Protection+186+50+BMS+5V+Micro+USB+1A+186+50+Lithium+Battery+Charging+Board&linkCode=gs3&linkId=957634db00eebaef6169a13464f34088&tag=circbasi-21&ref=as_li_ss_tl) |
| MCP1700-3302E 3.3V voltage regulator | 16 - 20 | [Link](https://www.amazon.es/AZDelivery-MCP23017-Expansor-bidireccional-interfaz/dp/B086W6ZQ36/ref=sr_1_2?dib=eyJ2IjoiMSJ9.jHvdlpaoDMq1UegLCFD1HThiE-tAmi9Y0FjJobEVVGnt5j5z2IJ9-WYL1Y30gHwgo-nHw3wAELHnkRUumeTxNgp-eDJT5HmHy41YhkdUQwcS7EqHeEToF27-_96GDvnjayi09-IIeM9Gz6hYWEUZYE0fz0NaCTpWRWYgwassqHd6PoQo9g7mfN0eff7bQmWaKzzwwMSqhBi5swrnAlRGmHU402p0sZ5hkfqCg7dpZp4.2RWReXyWL60JWdS56JdLZFTZQeOazl9ngkd73zmeViE&dib_tag=se&keywords=MICROCHIP%2BTECHNOLOGY%2BMCP1700-3302E%2FTO%2BMCP1700%2BSeries%2B250%2BmA%2B3.3%2BV%2BLow%2BDropout%2BPositive%2BVoltage%2BRegulator%2B-%2BTO-92-3%2B-%2B25%2Bitem(s)&linkCode=gs3&linkId=d0bcd6895ad98490119027404b917f5a&qid=1709469008&sr=8-2&th=1) |
| 6V DC, 500 mA solar panel* | 13 |[Link](https://www.amazon.es/NUZAMAS-Outdoor-Cargador-Bater%C3%ADa-Camping/dp/B073CDW1VZ/ref=sr_1_5?dib=eyJ2IjoiMSJ9.I2hHfkkPPnPgxT1QVuby6o9fpv_oj_UYb-sCu0BwvYMzHcVjTACohh6aQz7EQNHH1x_S_mR6M_bXI5e9ZjE2kpdeuUbk1BmTaVvWZPIQ3oaxAVTgRUyJUT1NDQmj4CTrO2I-9-CkF57T6VLp2IfAJ_GSG1HF5_ba_NBpZEPn8D_PKkNVUXZEnjMF6n3k2wEg41SjnCMUJeCtM3vSfHbXJLDZ9saeXvVfe6KZb8LhE8Ztgv2-n1SKPCBUa5WmMa9rYBb1k9roBttE_rhgemvITAUcdGjy04i5Fa6j44EQvxk.DeivZNw10diG9FhE-0n2ahvXIFDnekCHR0KuzliTGP0&dib_tag=se&keywords=Sunnytech+1pc+3.5w+6v+583ma+Mini+Solar+Panel+Module+Solar+System+Solar+Epoxy+Cell+Charger+DIY+B033&linkCode=gs3&linkId=d1df4e3088d10c13b16e6950e386a366&qid=1709469257&sr=8-5) |

### Batteries

These are some of the batteries that could be interesting to use:

| Name | Price (CHF) | URL |
| :---| :---: | ---: | 
| 8 * 3.7V 18650 Lithium Ion battery (2000 mAH or more)* | 2 (per battery)|[Link](https://www.amazon.com/AmazonBasics-Rechargeable-Batteries-8-Pack-Pre-charged/dp/B00CWNMV4G/ref=sr_1_1?crid=KYSGTI74BJM0&dib=eyJ2IjoiMSJ9.mJ6GgSojSIh4uLUXv6Mx6N1um2yNGpbrwuCKaYKhXZNKtoa4dDAgJ5f-Q2LBDvfzGtqrDnedTk0S4NMI9CI3BzRnZI2fMMxb08Fp4SdJw75CHWVSjBdlAPEZZkuY_FbrUB7LreJkpW2xoq6SfJx0b3bpZJ04eckX6OEKoixK4VgX7gd_Jtms8fv6gH_3Va7-FtF1bkAuU62gkvJMql4yfMCaBqxxCv69nlLgf9f14OU.GiLOg5ZI5THglz8DwDOw9hWKv3BAkiSaAUwgL_eS3VA&dib_tag=se&keywords=3.7V%2B18650%2BLithium%2BIon%2Bbattery&qid=1709469145&sprefix=3.7v%2B18650%2Blithium%2Bion%2Bbattery%2Caps%2C252&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1) |

**Note:** The components are yet to be decided as we do not know the precise amount of current needed for final build.

## Related projects

**Insight Robotics**:
Insight Robotics specializes in wildfire detection and monitoring solutions. They use thermal imaging and AI to detect fires early. Their system includes ground-based sensors and can integrate aerial imagery from drones for comprehensive monitoring and rapid response.

**Pano AI**:
Pano AI’s approach involves using AI-powered cameras mounted on high vantage points to detect smoke and fire. Their system can pinpoint the location of a fire, allowing for quick dispatch of firefighting resources. The use of drones for live streaming and further assessment could complement their existing infrastructure.


## User stories

The end user is aimed at forest fire guards and private forest owners that would want to be able to monitor and protect their land. They will be equiped with an app that will give them a live feed of the cameras and give them the exact geo-location of the fire.


