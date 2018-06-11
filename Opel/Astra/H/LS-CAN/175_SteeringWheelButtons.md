

## Steering wheel buttons and switches

| Address | Data    | Function | Byte1      | Byte2      | Byte3 | Byte4 | Byte5 | Byte6 | Byte7   | Byte8   |
| ------- | ----    | -------- | -----      | -----      | ----- | ----- | ----- | ----- | -----   | -----   |
| `175`   | 8 bytes | Complex  | Far lights | glass wash | *0x00*| *0x00* | turn lights | Buttons | left knob | right knob|

Functions are coded by bits, so use bit operations.

| Function | Byte1  | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| -------- | -----  | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| Far lights pull    | 0x08 | |  |  |  |  |  |  |
| Far lights push    | 0x20 | |  |  |  |  |  |  |
| glass wash OFF     |  | 0x00 |  |  |  |  |  |  |
| glass wash down    |  | 0x10 |  |  |  |  |  |  |
| glass wash push    |  | 0x?? |  |  |  |  |  |  |
| glass wash pull    |  | 0x?? |  |  |  |  |  |  |
| glass wash speed1  |  | 0xA0 |  |  |  |  |  |  |
| glass wash speed2  |  | 0xB0 |  |  |  |  |  |  |
| glass wash speed3  |  | 0xD0 |  |  |  |  |  |  |
| turn left 1        |  |  |  |  | 0x01 |  |  |  |
| turn right 1       |  |  |  |  | 0x02 |  |  |  |
| turn left 2        |  |  |  |  | 0x03 |  |  |  |
| turn right 2       |  |  |  |  | 0x04 |  |  |  |
| volume UP          |  |  |  |  |  | 0x01 |  | 0x01 |
| volume DOWN        |  |  |  |  |  | 0x02 |  | 0x1F |
| next / forward     |  |  |  |  |  | 0x04 |  |  |
| prev / backward    |  |  |  |  |  | 0x05 |  |  |
| left knob up       |  |  |  |  |  | 0x10 | 0x1F |  |
| left knob down     |  |  |  |  |  | 0x20 | 0x01 |  |
| left knob press    |  |  |  |  |  | 0x30 |  |  |
| next preset / ?    |  |  |  |  |  | 0x40 |  |  |
| AUX / CD / Radio   |  |  |  |  |  | 0x50 |  |  |
