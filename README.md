Air-Hammer-NG - A WPA Enterprise horizontal brute-force attack tool
==========
*Created by Michael "Wh1t3Rh1n0" Allen and reworked by Jan Phillip Schwietzer*

Introduction
------------
Air-Hammer-NG is an online brute-force attack tool for use against WPA Enterprise networks. Although WPA Enterprise is often considered "more secure" than WPA-PSK, it also has a much larger attack surface. While WPA-PSK networks have only one valid password, there may be thousands of valid username and password combinations which grant access to a single WPA Enterprise network. Further, passwords used to access WPA Enterprise networks are commonly selected by end users, many of whom select **extremely common passwords**.

Air-Hammer-NG has several advantages over current attacks against WPA Enterprise networks including:

* Client-less attacks
* Potentially larger attack surface
* Minimal hardware requirements

Installation
-----------------------
The recommended way to install Air-Hammer-NG is using `pipx` to ensure dependencies are isolated:

    sudo pipx install . --global

Once installed, the command `air-hammer-ng` will be available globally in your terminal.

Usage
-----
The `-h` or `--help` flags can be used to display Air-Hammer-NG's usage instructions.

```
$ air-hammer-ng --help
usage: air_hammer_ng.py -i interface -e SSID (-U USERNAME | -u USERFILE) [-P PASSWORD] [-p PASSFILE] [-d DOMAIN] [-s line] [-w OUTFILE] [-1] [-t seconds]

Perform an online, horizontal dictionary attack against a WPA Enterprise network.

options:
  -i interface  Wireless interface (default: None)
  -e SSID       SSID of the target network (default: None)
  -U USERNAME   Username to try with each password (default: None)
  -u USERFILE   Username wordlist (default: None)
  -P PASSWORD   Password to try on each username (default: None)
  -p PASSFILE   List of passwords to try for each username (default: None)
  -d DOMAIN     Domain to prepend (format: DOMAIN\username) (default: None)
  -s line       Optional start line to resume attack. May not be used with a password list. (default: 0)
  -w OUTFILE    Save valid credentials to a CSV file (default: None)
  -1            Stop after the first set of valid credentials are found (default: False)
  -t seconds    Seconds to sleep between each connection attempt (default: 0.5)
```
