## Chassis Data

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `100` | `Bus Wakeup` |
| `108` | `23:20:98:00:04:E5:00:00` | Motion | Mode¹ | **Speed>** | **<Speed decimal (km/h/1000)** | *0x00* | **RPM>** | **<RPM / 4** | *0x00* | *0x00* |
| `145` | `32:1:16:146:0:04:00:00` | Engine | ??? | ??? | ??? | **Coolant (°C-40)** | ? 0xA0=Run,0x00=Off  | *0x04* | *0x00* | ??? |
| `190` | **`00:00:F9:0B:00:01:17`** | ??? | *0x00* | *0x00* | **Mileage>** | **<Mileage>** | **<Mileage (km/64)** | *0x01* | ? (2) |
| `445` | `00:73` | Voltage | *0x00* | **Voltage / 8** |
| `500` | `00:5C` | Outdoor Temp | ? Most: 0x00 | **Out. Temp (°C/2-40)** |

¹ 0x13 = Standing, 0x23 = Driving
