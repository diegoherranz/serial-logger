Serial Logger
=============
Simple serial logger written in Python.

Logs everything received through a serial port (native or virtual) into a file whose name is the date and time when the log started, e.g. `2014-10-07T13.04.50.bin`.

Tested in Windows and Linux. It also works on the Raspberry Pi (tested on Raspbian).


Requirements
------------

- python 2.7 (or python 2.6 and argparse)
- pyserial

Basic usage
-----------
```
$ python serial_loger.py -d SERIAL_DEVICE -s SERIAL_SPEED
```

Defaults are `/dev/ttyUSB0` for `SERIAL_DEVICE` and `9600` (bps) for `SERIAL_SPEED`.

Linux example using a UART-USB adapter (`/dev/ttyUSB0`) and `9600` bps:
```
$ python serial_loger.py
Logging started. Ctrl-C to stop.
```

Windows example using `COM5` and 19200 bps:
```
$ python serial_loger.py -d COM5 -s 19200
Logging started. Ctrl-C to stop.
```

