
# Rowing tracker

## Prerequsities

- PC with Linux, Mac OS or Windows Subsystem for Linux (WSL)
- XIAO BLE Sense NRF52840
- Python 3.10+ installed on PC

## Setup


#### Flash MicroPython onto XIAO

- Connect XIAO to PC using USB-C cable
- Double tap `RESET` button to put XIAO into bootloader mode
- Copy .uf2 file from `binaries/`


#### Setup Python environment

Create virtual environment
```
python -m venv venv
```

Activate virtual environment

```
source venv/bin/activate
```

Install dependencies
```
pip install -r requirements.txt
```

#### Setup filesystem on XIAO

```
mpremote run firmware/make_vfs.py
```

#### Copy over Python files

```
mpremote cp firmware/*.py :lib
mpremote cp firmware/main.py :
```
