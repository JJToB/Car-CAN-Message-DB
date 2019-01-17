## Chassis Data

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `108` | `23:20:98:00:04:E5:00:00` | Motion | Mode¹ | Speed (km/h) | Speed decimal (km/h/1000) | *0x00* | RPM | RPM / 4 | *0x00* | *0x00* |
| `145` | `32:1:16:146:0:04:00:00` | Engine | ? Starter² | ? State³ | ? 0x10=Run, 0x01=Off | Coolant (°C-40) | ? 0xA0=Run,0x00=Off  | *0x04* | *0x00* | *0x00* |
| `500` | `00:73` | Voltage | *0x00* | Voltage / 8 |


¹ 0x13 = Standing, 0x23 = Driving
² 0x20 = Normal, 0x40 / 0x60 = During engine start
³ 0x00 = Off, Engine Start: 0x80, 0x81 then 0x01 until engine off
