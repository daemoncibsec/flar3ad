<h1 align="center">
  <img src="https://github.com/daemoncibsec/flar3ad/blob/main/flar3ad-logo.png" alt="flar3ad" width="1000px">
  <br>
</h1>

flar3ad is a tool that takes advantage of the CVE-2026-51031 to read files from a target server taking advantage of the `/v1` endpoint of FlareSolverr's API and using `driver.get()` function in order to exploit the vulnerability. Further explained in [xinyi's blog](https://xinyi234.github.io/2026/04/13/FlareSolverr-Server-Side-Request-Forgery-SSRF-Vulnerability-Report/).

## Installation

```bash
git clone https://github.com/daemoncibsec/flar3ad.git
cd flar3ad
python3 -m venv venv
source venv/bin/activate
pip install rich
pip install argparse
pip install requests
chmod +x flar3ad
```

To exit the venv:

```bash
deactivate
```

## Usage/Examples

Read the `/etc/passwd` file of the target server.


```bash
./flar3ad http://localhost:8191/ /etc/passwd
```

## Authors

- [@daemoncibsec](https://www.github.com/daemoncibsec)
