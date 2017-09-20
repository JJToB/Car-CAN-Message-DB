## Tire Pressure Monitoring System

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `684` | `46:0F:39:38:36:38` | Pressure | *0x46* | Sensor state¹ | /25=Bar-FL | /25=Bar-FR | /25=Bar-RL | /25=Bar-RR | - | - |
| `685` | `46:0F:49:49` | Battery | *0x46* | Sensor state¹ | Battery² | Battery² | - | - | - | - |

¹ Shows 0x0F when all sensors are sending data  
² Indicates the sensor Battery state, maybe B3=Front, B4=Read. 0x49 means Battery OK
