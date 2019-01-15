## Chassis Data

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `108` | `23:20:98:00:04:E5:00:00` | Motion | Mode¹ | Speed (km/h) | Speed decimal (km/h/1000) | *0x00* | RPM | RPM / 4 | *0x00* | *0x00* |

¹ 0x13 = Standing, 0x23 = Driving

