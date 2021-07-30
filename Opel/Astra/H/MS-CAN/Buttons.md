

# Radio buttons
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

##### Tested for CD70 and DVD90

| Button-ID | Button Description |
| --------- | ------------------ |
| `0x30` | Num 0 |
| `0x31` | Num 1 |
| `...` | ... |
| `0x39`| Num 9

# Steering wheel buttons

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `206` | `00:91:00` | release | *0x00* | Button-ID | Hold Time | - | - | - | - | - |
| `206` | `01:91:00` | press | *0x01* | Button-ID | Increments when hold | - | - | - | - | - |
| `206` | `08:91:00` | knob turn | *0x08* | Button-ID | *0x01* - UP, *0xFF* - DOWN | - | - | - | - | - |

## Button-IDs

| Button-ID | Button Description |
| --------- | ------------------ |
| `0x81` | Left Up Button |
| `0x82` | Left Down Button |
| `0x83` | Left Knob |
| `0x83` | Left Knob Button|
| `0x91` | Right Up Button (Next) |
| `0x92` | Right Down Button (Prev) |
| `0x93` | Right Knob (Volume) |



# AC Controller knobs

| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `208` | `01:17:00` | press | *0x01* | Button-ID | Increments when hold | - | - | - | - | - |
| `208` | `00:17:00` | release | *0x00* | Button-ID | Hold Time | - | - | - | - | - |
| `208` | `08:16:01` | knob turn | *0x08* | Button-ID | *0x01* - UP, *0xFF* - DOWN | - | - | - | - | - |

## Button-IDs

| Button-ID | Button Description |
| --------- | ------------------ |
| `0x16` | Center Knob |
| `0x17` | Center Knob Button |
