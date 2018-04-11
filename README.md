Madcoin-Core Revival Super Short Quick Command Guide:

1. - Login to your VPS instance as root
2. - ```git clone https://github.com/aznsquad/vps.git && cd vps```
3. - For ONE MN run: ```./install.sh -p mdcr```, for say, 3 MN, run: ```./install.sh -p mdcr -c 3```
4. - Place keygen ```nano /etc/masternodes/mdcr_n1.conf```
5. - Activate the masternode(s) by typing: ```/usr/local/bin/activate_masternodes_mdcr```
6. - If necessary type ```systemctl restart mdcr_n1``` to restart the node.
7. -  ```/usr/local/bin/madcoind -conf=/etc/masternodes/mdcr_n1.conf masternode status``` to check the status


Info:

+ the wallet and data are stored in ```/var/lib/masternodes/mdcrN/``` where n is the masternode number (1,2, 3...). You will find debug.log here.
+ A 1GB Vultr instance (5 USD one) should be able to serve 5-6 masternodes without issue. Use the top command to monitor mem / cpu usage to judge.
+ Want to add another masternode down the line? EZ PZ:  ```./install.sh -p mdcr -c 4``` (assume you had 3 setup before).
+ New coin update? Sure: ```./install.sh -p mdcr -c 4 -u``` (remember to set number after -c to the number of nodes you have running).


Bitcoin Donation address for aznsquad:

```
BTC 1SzFHBnsYPfcBXTRbPYDWmDWfEvhTankN
```

Feel free to use my reflink to signup and receive a bonus w/ vultr:
<a href="https://www.vultr.com/?ref=7282775"><img src="https://www.vultr.com/media/banner_2.png" width="468" height="60"></a>

---

## Installation

SSH to your VPS and clone the Github repository:

```bash
git clone https://github.com/aznsquad/vps.git && cd vps
```

Install & configure your desired master node with options:

```bash
./install.sh -p pivx
```

## Examples for typical script invocation

These are only a couple of examples for typical setups. Check my [easy step-by-step guide for [vultr](/docs/masternode_vps.md) that will guide you through the hardest parts.

**Install & configure 4 PIVX masternodes:**

```bash
./install.sh -p pivx -c 4
```

**Install 4 PIVX masternodes, update daemon:**

```bash
./install.sh -p pivx -c 4 -u
```

**Install 6 PIVX masternodes with the git release tag "tags/v3.0.5.1"**

```bash
./install.sh -p pivx -c 6 -r "tags/v3.0.5.1"
```

**Wipe all PIVX masternode data:**

```bash
./install.sh -p pivx -w
```

**Install 2 PIVX masternodes and configure sentinel monitoring:**

```bash
./install.sh -p pivx -c 2 -s
```

## References

```https://github.com/masternodes/vps.git```
```https://github.com/damiensgit/vps.git```

Bitcoin Donation address for aznsquad:

```
BTC 1SzFHBnsYPfcBXTRbPYDWmDWfEvhTankN
```
