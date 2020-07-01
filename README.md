# Canis Majoris Firmware

### Main Tasks

- Camera
	 - Writing driver code for Camera
	 - Taking photos every 2 seconds (at least 5 photos, 480x480p)
	 - Storing photos
-   ~~GPS ~~
    -   ~~Writing driver code for GPS module ~~
    -   ~~getting longitude and latitude information ~~
    
-   Data transmission
    -   Writing driver code for XBEE S1 (probably)
    -   Sending telemetric data  each second
        -   sending photos every 2 seconds
            
-   Telemetric information
    -   Battery voltage measurement IC **[?]**
    -   ~~Driver for BMP (180 or 280)~~ 
    -   Configuring Real Time Clock **[maybe use UTC time from GPS?] **
    -   Measuring number of cycles of propeller **[?]**
        
-   Main Driver Code
    -   Configuring FREERTOS    
    -   3 main threads:
        -   data acquisition (telemetry info)            
        -   data processing
        -   data sending
    -   additional threads:
        -   satellite balance
        -   camera handler

### List of parts
- STM32F103C8T6 (microcontroller)
- XBEE S1 (for radiotransmission)
- MPU 6050 (gyrosensor)
- BMP280 (pressure sensor for altitude measurement)
***
- Soldering wire
- Battery 
- GPS module
- XBEE antenna
- Brushless DC motor *
- ESC - electronic speed controller *
- SD card
- SD card slot
- Camera 
- Propeller
- ...

\* = maybe instead use passive landing 
#### 21.01.2020
