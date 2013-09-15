Protocol v.01

Describes how data is en/decoded for transmission via a visible light source.
Different schemas to defines increasing complexity, reliability, and likely increasing bandwidth.
Receivers should be backward compatible to allow for a variety of different schema transmitters to use the defined protocols.


Schema 1
=========
* One way transmission
* No FEC, error checking, parity, or erasure handling

Physical Layer
--------------
* 2 Color (White, Black)
* Large single color block
* Minimum display time of X milliseconds

Data Link Layer
---------------
* White = 1
* Black =  0
* No parity, no error checking, no framing

Schema 2
=========
* One way transmission
* No FEC, error checking, parity, or erasure handling
* Quaternary

Physical Layer
--------------
* 4 Color (Blue, White, Red, Black)
* Large single color block
* Minimum display time of X milliseconds

Data Link Layer
---------------
* Black = 0
* Blue = 1
* Red = 2
* White = 3
* No parity, no error checking, no framing
* Base 4
* Frame
*   Start [0,3,0,3]
*   Data  [d1,d2,d3,parity] xN
*   End   [1,2,1,2] 

Decoding
--------
Start and End transitions used to determine clocking / duration of each quaternary number.  Although standard timing should be used.

Schema 3
========
* Forward Error Correction

Future Schema
=============
* Turbo codes (http://itpp.sourceforge.net/devel/classitpp_1_1Turbo__Codec.html)
* Large number of colors and/or transitions   (Blue -256, Red +256). Luminance not taken into account



