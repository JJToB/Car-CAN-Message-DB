

## Radio buttons
##### Tested for CD30, CD70 and DVD90

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `201` | `00:31:00` | release | *0x00* | Button-ID | Hold Time | - | - | - | - | - |
| `201` | `01:31:00` | press | *0x01* | Button-ID | Increments when hold¹ | - | - | - | - | - |
| `201` | `08:6A:00` | knob turn | *0x08* | *0x6A* | Turn-Direction | - | - | - | - | - |

¹ The counter is following the frame's period (100ms). The counter increases up to 0xFF.

## Button-IDs
##### Tested for CD30

| Button-ID | Button Description |
| --------- | ------------------ |
| `0x01` | BC |
| `0x6F` | OK |
| `0x6D` | Left |
| `0x6C` | Right |
| `0xE0` | FM or CD |
| `0xFF` | Settings |

## Steering wheel buttons

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `206` | `00:91:00` | release | *0x00* | Button-ID | Hold Time | - | - | - | - | - |
| `206` | `01:91:00` | presse | *0x01* | Button-ID | Increments when hold | - | - | - | - | - |
