[![Build Status](https://travis-ci.org/la5nta/pat.svg?branch=master)](https://travis-ci.org/la5nta/pat)

## Pat

Pat is a cross platform Winlink client with basic messaging capabilities.

It is the primary sandbox/prototype application for the [wl2k-go](https://github.com/la5nta/wl2k-go) project, and provides both a command line interface and a responsive (mobile-friendly) web interface.

It is mainly developed for Linux, but are also known to run on OS X, Windows and Android.

#### Features
* Message composer/reader (basic mailbox functionality).
* Auto-shrink image attachments (EXPERIMENTAL).
* Post position reports with location from local GPS, browser location or manual entry.
* Rig control (using hamlib) for winmor PTT and QSY.
* CRON-like syntax for execution of scheduled commands (e.g. QSY or connect).
* Built in http-server with web interface (mobile friendly).
* Git style command line interface.
* Listen for P2P connections using multiple modes concurrently.
* AX.25, telnet, WINMOR and ARDOP support.
* Experimental gzip message compression (See "Gzip experiment" below).

##### Example
```
martinhpedersen@duo:~$ pat interactive
> listen winmor,telnet-p2p,ax25
2015/02/03 10:33:10 Listening for incoming traffic (winmor,telnet-p2p,ax25)...
> connect winmor:///LA3F
2015/02/03 10:34:28 Connecting to winmor:LA3F...
2015/02/03 10:34:33 Connected to WINMOR:LA3F
RMS Trimode 1.3.3.0 Follo.SE Oslo. Pactor & Winmor Hybrid Gateway
LA5NTA has 117 minutes remaining with LA3F
[WL2K-2.8.4.8-B2FWIHJM$]
Wien CMS via LA3F >
>FF
FC EM FOYNU8AKXX59 260 221 0
F> 68
1 proposal(s) received
Accepting FOYNU8AKXX59
Receiving [//WL2K test til linux] [offset 0]
>FF
FQ
Waiting for remote node to close the connection...
> _
```

### Gzip experiment

Gzip message compression has been added as an experimental B2F extension, as an alternative to LZHUF. The feature can be enabled by setting the environment variable `GZIP_EXPERIMENT=1` at runtime.

For more information, see <https://github.com/la5nta/wl2k-go#gzip-experiment>.

## Copyright/License

Copyright (c) 2014-2016 Martin Hebnes Pedersen LA5NTA

### Contributors (alphabetical)

* LA3QMA - Kai Günter Brandt
* LA5NTA - Martin Hebnes Pedersen

## Thanks to

The JNOS developers for the properly maintained lzhuf implementation, as well as the original author Haruyasu Yoshizaki.

The paclink-unix team (Nicholas S. Castellano N2QZ and others) - reference implementation

Amateur Radio Safety Foundation, Inc. - The Winlink 2000 project

F6FBB Jean-Paul ROUBELAT - the FBB forwarding protocol

_Pat/wl2k-go is not affiliated with The Winlink Development Team nor the Winlink 2000 project [http://winlink.org]._
