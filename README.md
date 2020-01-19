# Canis Majoris Firmware

### Main Tasks

- Camera
	 - Writing driver code for Camera [ camera.h, camera.c ]
	 - Taking photos every 2 seconds (at least 5 photos, 480x480p)
	 - Storing photos
-   GPS
    -   Writing driver code for GPS module
    -   getting longitude and latitude information
    
-   Data transmission
    -   Writing driver code for XBEE S1 (probably)
    -   Sending telemetric data  each second
        -   sending photos every 2 seconds
            
-   Telemetric information
    -   Battery voltage measurement IC ?
    -   Driver for BMP (180 or 280)
    -   Configuring Real Time Clock
    -   Measuring number of cycles of propeller (?)
        
-   Main Driver Code
    -   Configuring FREERTOS    
    -   3 main threads:
        -   data acquisition (telemetry info)            
        -   data processing
        -   data sending
    -   additional threads:
        -   satellite balance
        -   camera handler

### List of electronics
- STM32F103C8T6 (microcontroller)
- XBEE S1 (for radiotransmission)
- MPU 6050 (gyrosensor)
- BMP280 (pressure sensor for altitude measurement)
- ...

### Telemetric data packet format 
 
  - [ID] 
  - [Uptime]
  - [N of packets] 
  - [Voltage] 
  - [Altitude] 
  - [Velocity]
  - [Latitude]
  - [Longtitude]
  - [Photo Info]
  - [Propeller]
  - [Real time for dispatch] 
  - [N of photos taken] 
  - [N of photos sent] (optional)




19.01.2020
