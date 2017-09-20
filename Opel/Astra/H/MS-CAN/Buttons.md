

| Address | Data | Function | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- |
| <td colspan=3>**Radio buttons**</td> |
| `02 01` | `00 31 00` | Released | 0=Release | Button-ID | Static 0 | - | - | - |
| `02 01` | `01 31 00` | ressed | 1=Press | Button-ID | Increments when hold | - | - | - |
| **Steering wheel buttons** ||
| `02 06` | `00 91 00` | Released | 0=Release | Button-ID | Static 0 | - | - | - |
| `02 06` | `01 91 00` | Pressed | 1=Press | Button-ID | Increments when hold | - | - | - |
