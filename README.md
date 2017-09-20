# Car-CAN-Message-DB
A Database containing all discovered CAN-BUS messages in cars


This intents to be a List of discovered CAN-BUS messages in cars for various functions.

The Structure loos as follows (with examples):

| Make | / | Model | / | Verion | / | Bus | / | Component.md |
| ---- | - | ----- | - | ------ | - | --- | - | ------------ |
| BMW | / | 3-Series | / | E90 | / | K-CAN | / | Instrument.md |
| Opel | / | Astra | / | H | / | MS-CAN | / | Body.md |


The .md files itself should look like this:


>## Chassis Data
>
>| Address | Data | Function | Byte1 | Byte2 | Byte3 | Byte4 | Byte5 | Byte6 | Byte7 | Byte8 |
>| ------- | ---- | -------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
>| `180` | `46:01:10:0B:F1:6F:37:FF` | Time | *0x46* | *0x01* | Year | Month | 5B:Day, 3b:Hour | 2b:Hour, 6b:Minute | Second | **??** |
>| `188` | `46:0A:F3:62:F6:D4` | Distance | *0x46* | IGN 00/0A | 2B\*1.5748=cm¹ | <- | 2B\*1.5748=cm¹ | <- | - |
>
>¹ The two Distance Values in Byte 4+5 and 6+7 might be different wheels as they slightly differ while driving.  


- The Adress and Data Fiels are Monospaced (by \`) 
- The Fields for each Byte includes a short Description of that byte
- Fields that belong to the Byte before are markety by <-
- Longer Descriptions are added as footnotes
- Static fields are marked by the static italic value (by \*)
