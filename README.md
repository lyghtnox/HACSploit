# HACSploit

POC for the vulnerability impacting HACS < 1.10.0

This script will check the vulnerability of a given instance and try to craft an admin token to log in.

Blog post [here](https://lyghtnox.gitlab.io/posts/hacs-exploit/).

Please use this tool only on YOUR OWN Home Assistant instance.

## Installation

```
git clone https://github.com/lyghtnox/HACSploit
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Usage

```
$ python exploit.py -h
usage: exploit.py [-h] host port

Exploit a vulnerability in HACS < 1.10.0 to gain admin access to an Home Assistant instance.

positional arguments:
  host        IP of the HASS instance
  port        port of the HASS instance

optional arguments:
  -h, --help  show this help message and exit

```

If the exploit is successful, the script will print an access token. Set this token in the local storage of your browser for the given instance with the key `hassTokens`. Then navigate to the root of the instance (`http://host:port`). You should now be logged in as admin.