## Chassis Data

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `180` | `46:01:10:0B:F1:6F:37:FF` | Time | *0x46* | *0x01* | Year | Month | 5B:Day, 3b:Hour | 2b:Hour, 6b:Minute | Second | ?? |
| `188` | `46:0A:F3:62:F6:D4` | Distance | *0x46* | IGN 00/0A | 2B\*1.5748=cm¹ | <- | 2B\*1.5748=cm¹ | <- | - |
| `682` | `46:01:75` | Sensor Temp | *0x46* | *0x01* | /2-40=°C² | - | - | - | - |
| `683` | `46:01:76` | Display Temp | *0x46* | *0x01* | /2-40=°C³ | - | - | - | - |
| `68C` | `46:01:6B` | Fuel Level | *0x46* | *0x01* | 94-(X/2)=l⁴ | - | - | - | - |

¹ The two Distance Values in Byte 4+5 and 6+7 might be different wheels as they slightly differ while driving.  
² Outdoor Temperature reported by sensor  
³ Outdoor Temperature shown on display  
⁴ Gas tank level, calculation depends on sensor, sometimes inverted


## Engine Data

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `4E8` | `46:0F:0C:50:19:0A:02` | Motion | *0x46* | ?? | RPM | RPM | Speed | ? | Direction¹ | - |
| `4EC` | `46:07:3C:29:00` | Engine Temp | *0x46* | IGN 00/07 | -40=°C | ?? | - | - | - | - |
| `4ED` | `46:02:41:43` | Fuel Injection | *0x46* | IGN² | 2B Injections³ | <- | - | - | - | - |
| `4EE` | `46:03:05:06` | Range | *0x46* | Low-range⁴ | 2B\*0.5=km Range | <- | - | - | - | - |

¹ 0x01=Stand, Bit2:Moving, Bit3:Reverse. Not sure about the state between standing and moving. Maybe clutch-state etc.  
² 0x00=Ignition Off, 0x02:Engine runnung, 0x03=Ignition On  
³ Number of injections, a value of 0xFFFF are approximately 2 liters at my Z16XEP engine.  
⁴ Low range warning 0x03=OK, 0x00=Low-range  
