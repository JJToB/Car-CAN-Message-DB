## Chassis Data

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `100` | `Bus Wakeup` |
| `108` | `23:20:98:00:04:E5:00:00` | Motion | Mode¹ | **Speed>** | **<Speed decimal (km/h/1000)** | *0x00* | **RPM>** | **<RPM / 4** | *0x00* | *0x00* |
| `145` | `32:1:16:146:0:04:00:00` | Engine | ??? | ??? | ??? | **Coolant (°C-40)** | ? 0xA0=Run, 0x00=Off  | *0x04* | *0x00* | ??? |
| `190` | `00:00:F9:0B:00:01:17` | ??? | *0x00* | *0x00* | **Mileage>** | **<Mileage>** | **<Mileage (km/64)** | *0x01* | ? (2) |
| `360` | `00:00:40` |  Clutch | *0x00* | *0x00* | **0x00=Norm, 0x40=Clutch pressed** |
| `445` | `00:73` | **Outdoor Temp** | *0x00* | **Out. Temp (°C/2-40)** |
| `500` | `00:5C` | **Voltage** | ??? | **Voltage (V/8)** |
| `530` | `11:11:34:34:38:3A:28:29` | TPMS | State F | State R | **FL (Bar/25)** | **FR (Bar/25)** | **RL (Bar/25)** | **RR (Bar/25)** | 0x28=OK | 0x29=ON |
                                                                                                         
¹ 0x13 = Standing, 0x23 = Driving
