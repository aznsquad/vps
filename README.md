## Installation

Using Artax as an example, SSH to your VPS and clone the Github repository as root:

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
git clone https://github.com/aznsquad/vps.git && cd vps
```

Install & configure your desired masternode with options:

```bash
./install.sh -p xax
```

or Install 2 more masternodes:
```bash
./install.sh -p xax -c 2
```

Place keygen in:
```bash
nano /etc/masternodes/xax_n1.conf
```

Activate the masternode(s) by typing:
```bash
/usr/local/bin/activate_masternodes_xax
```

If necessary to restart the node, type:
```bash
systemctl restart xax_n1
```

To check the masternode status:
```bash
/usr/local/bin/madcoind -conf=/etc/masternodes/xax_n1.conf masternode status
```

To wipe the masternode:
```bash
./install.sh -p xax -w
```

**FYI:**

Wallet and data are stored in:
```cd /var/lib/masternodes/mdcrN/```
where n is the masternode number (1,2, 3...). You will find debug.log here.

A 512M Vultr instance ($2.50/mo) should be able to serve 5-6 masternodes without issue.

Coin update:
```./install.sh -p mdcr -c 4 -u``` (remember to set number after -c to the number of nodes you have running).

---

Bitcoin Donation address for aznsquad:

BTC ```1SzFHBnsYPfcBXTRbPYDWmDWfEvhTankN```


Feel free to use my reflink to signup and receive a bonus w/ vultr:
<a href="https://www.vultr.com/?ref=7282775"><img src="https://www.vultr.com/media/banner_2.png" width="468" height="60"></a>

---

## Examples for typical script invocation

These are only a couple of examples for typical setups. Check my [easy step-by-step guide for [vultr](/docs/masternode_vps.md) that will guide you through the hardest parts.


**Install 4 Artax masternodes, update daemon:**

```bash
./install.sh -p xax -c 4 -u
```

**Install 6 Artax masternodes with the git release tag "tags/v3.0.5.1"**

```bash
./install.sh -p xax -c 6 -r "tags/v3.0.5.1"
```

**Install 2 Artax masternodes and configure sentinel monitoring:**

```bash
./install.sh -p xax -c 2 -s
```

## References

```https://github.com/masternodes/vps.git```

---

Bitcoin Donation address for aznsquad:

BTC ```1SzFHBnsYPfcBXTRbPYDWmDWfEvhTankN```
