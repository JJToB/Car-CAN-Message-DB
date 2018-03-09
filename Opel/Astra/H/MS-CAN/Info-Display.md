
## Info Display
##### Tested for GID and CID

The massages to the display are larger than 8-Byte Packets and use the [ISO-15765-2](https://en.wikipedia.org/wiki/ISO_15765-2) protocol to pack the message in multiple packets.
The datablock itself contains of a two Byte Command, one Byte payload size, one message type¹ Byte and multiple sub packets:
- ID - Identifies the displayrow (10: Title, 11: Album, ... see below)
- Number of Characters for this ID
- Characters as UTF-16²

¹ The message type describes what kind of Information is send (Main Screen, Menu, Infobox, AC, ...)

² The UTF-16 Support is very limited. The only extended chars I discovered are 0x2780-0x2788 for &#x2780;-&#x2788;  


For Example, this is A packet dump, displaying "Aux" in the center line of the Display:
```
6C1 # 10 2E C0 00 2B 03 01 01
2C1 # 30 00 00 00 00 00 00 00
6C1 # 21 00 20 23 03 00 41 00
6C1 # 22 75 00 78 10 0A 00 1B
6C1 # 23 00 5B 00 66 00 53 00
6C1 # 24 5F 00 67 00 6D 00 41
6C1 # 25 00 75 00 78 11 01 00
6C1 # 26 20 12 01 00 20 01 00
```

The above Package is analyzed as follows:

![alt text](https://github.com/Trueffelwurm/Car-CAN-Message-DB/raw/master/Opel/Astra/H/MS-CAN/CID-AUX-Message.png "Logo Title Text 1")

These are the discovered message types:

| Type | Effect |
| ---- | ------ |
| `01` | FM section in audio source menu |
| `03` | Main screen: audio |
| `05` | CD section in audio source menu |
| `07` | Main screen: phone |
| `09` | Main screen: satnav |
| `0A` | AC section |

And this are the Specific IDs for each message type:


| Type | ID | Field |
| ---- | -- | ----- |
| `01` | `01` | Radio station Name |
| `01` | `02` | Radio freqency |
| `01` | `03` | Scan-mode (i.e. "Autostore") |
| ---- | ---- | -------------|
| `03` | `01` | ??? (Sends "Audio")|
| `03` | `02` | ??? Menu item name? (Sends "Aux")|
| `03` | `10` | Song title |
| `03` | `11` | Album title |
| `03` | `12` | Artist |
| `03` | `23` | ??? Menu item name? (Sends "Aux") |
| ---- | ---- | -------------|
| `07` | `02` | Phone carrier name |
| ---- | ---- | -------------|
| `09` | `02` | Current height (String)¹ |
| `09` | `02` | Current location (String coordinates)¹ |
| `09` | `30` | Satnav state |
| `09` | `33` | Current location (Road name)|
| ---- | ---- | -------------|
| `0A` | `23` | AC temperature |
| `0A` | `24` | AC Position² |
| `0A` | `25` | AC mode ("ECO" or empty) |
| `0A` | `26` | AC fan level³ |

¹Only sent after "Info" button pressed

²Special-Chars 0xE051 to 0xE057 are position arrows. The Seat-Icon appers if automatically if one special char is sent.

³The FAN-Icons is the special char 0xE050
