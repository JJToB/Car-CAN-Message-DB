## All Values seen on the LS-CAN (Also known as SW-CAN - SingleWire or GMLAN)

|  Address  |   Data                        | Function               | When?  | Byte1             | Byte2             | Byte3             | Byte4             | Byte5             | Byte6             | Byte7             | Byte8             |
| --------- | ----------------------------- | ---------------------- | ------ | ----------------- |------------------ |------------------ |------------------ |------------------ |------------------ |------------------ |------------------ |
|   `040`   |   `00:00:C8:03:06:80`         |   ???                  | ?      | *0x00*            | ? (4)             | *0xC8*            | *0x03*            | ? (3)             | ? (4)             |
|   `048`   |   `01:01:61:D0:00:00`         |   ???                  | ?      | *0x01*            | *0x01*            | *0x61*            | *0xD0*            | *0x00*            | *0x00*            |
|   `050`   |   `01:02:61:D0:00:00`         |   ???                  | ?      | *0x01*            | *0x02*            | *0x61*            | *0xD0*            | *0x00*            | *0x00*            |
|   `068`   |   `01:20:61:D0:00:00`         |   ???                  | ?      | *0x01*            | *0x20*            | *0x61*            | *0xD0*            | *0x00*            | *0x00*            |
|   `090`   |   `00:00:71:00:00:00`         |   ???                  | ?      | *0x00*            | *0x00*            | ? (2)             | *0x00*            | *0x00*            | *0x00*            |
| **`100`** |                               | **Bus Wakeup**         | Unlock |
| **`108`** | **`23:20:98:00:04:E5:00:00`** | **Speed/RPM**          |   50ms | ? (10)            | **Speed**         | **Speed**         | *0x00*            | **RPM**           | **RPM**           | *0x00*            | *0x00*            |
| **`110`** | **`00:B4:92:B4:14`**          | Distance Traveled      |  100ms | ? (4)             | **Wheel FL**      | **Wheel FL**      | **Wheel FR**      | **Wheel FR**      |
|   `115`   |   `0E`                        | Break Switch or Light  |~1000ms | ? (9)             |
|   `11A`   |   `C0:00:40:80:01:00:00`      |   ???                  |~1500ms | *0xC0*            | *0x00*            | *0x40*            | ? (2)             | *0x01*            | *0x00*            | *0x00*            |
| **`130`** | **`00:13:A6:00:00:00:00`**    | **Fuel Injection**     | ~200ms | ? (4)             | **Fuel**          | **Fuel**          | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `135`   |   `3C:06:61:D0`               |   ???                  | ?      | ? (3)             | ? (2)             | *0x61*            | *0xD0*            |
|   `145`   |   `20:00:01:28:00:04:00:00`   | Engine                 |  100ms | Status            | Status            | Status            | **Coolant**       | Status            | **CruseControl**            | *0x00*            | *0x00*            |
|   `155`   |   `00:20`                     |   ???                  |  100ms | *0x00*            | ? (18)            |
|   `160`   |   `02:10:C8:03`               |   ???                  | ?      | *0x02*            | ? (3)             | *0xC8*            | *0x03*            |
|   `170`   |   `20:00:00:00`               |   ???                  | ?      | ? (8)             | ? (2)             | 0x03=KeyIn             | *0x00*            |
|   `175`   |   `00:00:00:00:00:00:00:00`   | **Column switch**      | Event  | ? (4)             | ? (5)             | ? (6)             | ? (2)             | *0x00*            | ? (3)             | *0x00*            | ? (2)             |
|   `188`   |   `01:FF:E0`                  |   ???                  | ?      | ? (3)             | ? (72)            | ? (17)            |
| **`190`** | **`00:00:F9:0B:00:01:17`**    | **Mileage**            | 1000ms | *0x00*            | *0x00*            | **Mileage**       | **Mileage**       | **Mileage**       | *0x01*            | ? (3)             |
|   `230`   |   `00:50:10:00:00:00:00`      |   ???                  | ?      | ? (2)             | ? (2)             | ? (3)             | *0x00*            | *0x00*            | ? (2)             | *0x00*            |
| **`235`** |   `00:FF`                     |  **LED Brightness**    | 1000ms | *0x00*            | **LED-Bright.**   |
|   `250`   |   `06:AE:02:FF:30:FF:10:FF`   |   ???                  | ?      | *0x06*            | *0xAE*            | *0x02*            | *0xFF*            | *0x30*            | *0xFF*            | *0x10*            | *0xFF*            |
|   `251`   |   `06:AE:01:3F`               |   ???                  | ?      | *0x06*            | *0xAE*            | *0x01*            | *0x3F*            |
|   `255`   |   `05:AE:07:01:80:00:00:00`   |   ???                  | ?      | *0x05*            | *0xAE*            | ? (2)             | *0x01*            | ? (2)             | *0x00*            | *0x00*            | *0x00*            |
|   `260`   |   `00:00:00`                  | **Turn signal**        | Event  | ? (5)             | ? (3)             | ? (2)             |
|   `275`   |   `3C:04:0E:FF:7F`            |   ???                  | ?      | ? (2)             | ? (2)             | ? (8)             | ? (2)             | ? (8)             |
|   `280`   |   `DC:06:43:00:FF`            |   ???                  | ?      | *0xDC*            | *0x06*            | *0x43*            | *0x00*            | *0xFF*            |
|   `285`   |   `00:00:00:00:00`            |   ???                  | ?      | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `295`   |   `02:AB:DE:9D`               |   ???                  | ?      | ? (4)             | ? (27)            | ? (11)            | ? (61)            |
|   `305`   |   `00:00:00:00:10:10:00`      |   ???                  | ?      | *0x00*            | *0x00*            | ? (2)             | ? (2)             | ? (2)             | ? (3)             | *0x00*            |
|   `315`   |   `00`                        |   ???                  | ?      | *0x00*            |
|   `330`   |   `08`                        |   ???                  | ?      | *0x08*            |
|   `340`   |   `00:00`                     |   ???                  | ?      | *0x00*            | *0x00*            |
|   `350`   |   `02:01:78:00`               |   ???                  | ?      | ? (14)            | ? (2)             | ? (54)            | ? (3)             |
|   `360`   |   `00:00:40`                  | Clutch                 | ?      | *0x00*            | *0x00*            | **Clutch**        |
|   `370`   |   `20:02:00:00:00:00:00:00`   | CheckControl?          | ?      | *0x20*            | 0x03=Washwater    | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `375`   |   `00:A0`                     |   **Fuel level**       | 40ms   | *0x00*            | **Fuel**          |
|   `380`   |   `00`                        |   ???                  | ?      | *0x00*            |
|   `400`   |   `21:00:00:00:00`            |   ???                  | ?      | ? (3)             | *0x00*            | ? (2)             | *0x00*            | *0x00* |
|   `425`   |   `02`                        |   ???                  | ?      | ? (3)             |
|   `430`   |   `03:FF:FF:00`               |   ???                  | ?      | ? (7)             | *0xFF*            | ? (44)            | *0x00*            |
| **`440`** | **`80:90:B0:00:00:78:10:13`** | **System Time**        | 1000ms | Hours             | Minutes           | Seconds           | ? (2)             | *0x00*            | *0x78*            | *0x10*            | *0x13*            |
| **`445`** | **`00:73`**                   | **Outdoor Temp**       | 1000ms | 0x00/?            | **Out. Temp**     |
|   `450`   |   `00:0A:00`                  |   ???                  | ?      | ? (2)             | *0x0A*            | ? (5)             |
| **`500`** |   `00:5C`                     | **Voltage**            | 1500ms | *0x00*            | **Volt**          |
|   `520`   |   `00:80:00:00:00:00:00:00`   |   ???                  | 1000ms | *0x00*            | *0x80*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
| **`530`** | **`11:11:34:34:38:3A:28:29`** | **TPMS**               | 1000ms | State F           | State R           | Bar FL            | Bar FR            | Bar RL            | Bar RR            | 0x28=OK           | 0x29=ON           |
|   `531`   |   `10:70:32:11:11`            |   ???                  | ?      | ? (12)            | ? (21)            | ? (12)            | ? (48)            | ? (3)             |
|   `5E8`   |   `81:00:00:74:10:00:00:00`   |   ???                  | ?      | *0x81*            | *0x00*            | *0x00*            | ? (35)            | *0x10*            | *0x00*            | *0x00*            | *0x00*            |
|   `625`   |   `00:08:00:00:00:00:00:00`   |   ???                  | ?      | ? (2)             | ? (5)             | ? (6)             | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `626`   |   `00:11:00:00:00:00:00:00`   |   ???                  | ?      | ? (2)             | *0x11*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `630`   |   `00:00:10:00:00:00:00:00`   |   ???                  | ?      | *0x00*            | *0x00*            | *0x10*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `631`   |   `00:08:00:00:00:00:00:00`   |   ???                  | ?      | ? (2)             | ? (3)             | ? (4)             | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `635`   |   `00:08:40:00:00:00:00:00`   |   ???                  | ?      | ? (2)             | ? (2)             | ? (3)             | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `637`   |   `01:00:10:00:00:00:00:00`   |   ???                  | ?      | *0x01*            | *0x00*            | *0x10*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `650`   |   `02:EE:02:00:00:00:00:00`   |   ???                  | ?      | *0x02*            | *0xEE*            | *0x02*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `651`   |   `02:EE:01:00:00:00:00:00`   |   ???                  | ?      | *0x02*            | *0xEE*            | *0x01*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |
|   `655`   |   `01:60:07:00:00:00:00:00`   |   ???                  | ?      | ? (2)             | ? (2)             | ? (2)             | *0x00*            | *0x00*            | *0x00*            | *0x00*            | *0x00*            |

*Italic* Values seam to bee fixed as no other values then the stated ones where ever seen.
This could also be a fault indicator which never triggerd in my car.  
**Bold** Values are already identified and explained on the specific page. Bold IDs are explained in detail below.  
The parenthesized values are the amount of different values seen.  



## 0x100 Wake up Bus
This messages is sent when the bus is offline and will wake up all attached devices  


## 0x108 Speed and RPM
This are some data from the engine  
*Byte 1*: Unknown, 10 different values are seen here.  
*Byte 2+3*: Speed (Divide _by 128_)  
*Byte 4*: Always `0x00`  
*Byte 5+6*: RPM  
*Byte 6+7*: Always `0x00`   
Example: `23:20:98:00:04:E5:00:00`  
Speed: **0x2098** = 8344 / _128_ = **65.1875 km/h**  
RPM: **0x04E5** = **1253 rpm**  


## 0x110 Distance traveled
Traveled distance per driven wheel, incrementing  
*Byte 1*: Unknown, 4 differen values are seen  
*Byte 2+3*: Traveled Distance for front left wheel  
*Byte 4+5*: Traveled Distance for front right wheel  
One increment is _1.5748 cm_  
Example: `00:B4:92:B4:14`  
Left: **0xB492** = 46226 * _1.5748_ = 72796.7048 cm = **727.96 m**  
Right: **0xB414** = 46100 * _1.5748_ = 72598.2800 cm = **725.98 m**  
A full cycle of the 16 bit integer are 1032 m.    


## 0x130 Fuel injection
*Byte 1*: Unknown, 4 differen values are seen  
*Byte 2+3*: Increments every fuel injection  
*Byte 4-7*: Always `0x00`  
At my 1.6l Engine, one increment is _0.03054 ml_  
Example: `00:13:A6:00:00:00:00`  
Injected: **0x13A6** = 5030 * _0.03054_ = **153,62 ml**  
A full cycle of the 16 bit integer are about 2 liters.  


## 0x145 Engine Data
Byte 1:  
* `0x00`: Engine Running  
* `0x20`: Ignition ON, engine not running  
* `0x40`/`0x60`: Engine start  

Byte 2:  
* `0x00`: Engine off
* `0x01`: Engine running  
* `0x80`/`0x81`: Engine starting  

Byte 3:  
* `0x01`: Engine off  
* `0x10`: Engine running  

Byte 4: Coolant (°C _- 40_)  

Byte 5:  
* `0x00`: Engine off  
* `0xA0`: Engine running  

Byte 6: 
* `0x04`: Cruisecontrol inactive 
* `0x06`: Cruisecontrol active

Byte 7+8: Always `0x00`  
Example: `20:00:01:26:00:04:00:00`  
Coolant: **0x28** = 38 - _40_ = **-2 °C**  


## 0x175 Colums Switches
*Byte 1,2,4,5,7,8*: No other values than `0x00` seen so far.  
*Byte 3*: Left column switch (Turn signal):  
* `0x01`: half pressed down  
* `0x02`: half pressed up  
* `0x03`: fully pressed  down  
* `0x04`: fully pressed up  

*Byte 6*: Right columns switch (Whiper control):  


## 0x235 LED Brightness
*Byte 1*: Always `0x00`  
*Byte 2*: LED Brightness from 0x01 to 0xFF. 0x00 is off / day mode (Instrument at full Brightness)  


## 0x375 Fuel Level
*Byte 1*: Always `0x00`  
*Byte 2*: Fuel Level, value depends on Sensor  
Example: `00:A0`  
Fuel: **0xA0** = 94 - ( _160_ / 2 ) = **14.0l**  

## 0x440 Time
*Byte 1*: Hours  
*Byte 2*: Minutes  
*Byte 3*: Seconds / 4  

| **`440`** | **`80:90:B0:00:00:78:10:13`** | **System Time**     
## 0x260
Seams to be TurnSignal control  

| Byte1 | Byte2 | Byte3 | Meaning |
| --- | --- | --- | --- |
| `0x00` | `0x00`| `0x00` | Turn signals off (Sent twice when indicator is turned off) |
| `0x25` | `0x43`| `0x7F` | Left turn signal (Sent every time the indicator lights up) |
| `0x3A` | `0x43`| `0x7F` | Right turn signal (Sent every time the indicator lights up) |
| `0x5F` | `0x32`| `0x7F` | Flash hazard lights (Sent once when locking the car) |
| `0x7F` | `0x32`| `0x7F` | Flash hazard lights twice (Sent once when unlocking the car) |
