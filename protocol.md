
Describes how data is en/decoded for transmission via a visible light source.
Different schemas to defines increasing complexity, reliability, and likely increasing bandwidth.
Receivers should be backward compatible to allow for a variety of different schema transmitters to use the defined protocols.


Schema 1
=========
* One way transmission
* No error checking, parity, or erasure handling

Physical Layer
--------------
4 Color (Blue, White, Red, Black)
Large single color block
Minimum display time of X milliseconds

Data Link Layer
---------------
Blue/White = 1
Red/Black =  0
No parity, no error checking, no frames

Schema 2
=========
