# IPTABLES

## INSTALL

`└─ $ ▶ sudo apt-get update`

`└─ $ ▶ sudo apt-get install iptables`

## Check iptables status

`└─ $ ▶ sudo iptables -L -v`

---

## Configuration :

    ACCEPT – accepts packet to pass through
    DROP – does not accept packet to pass through
    RETURN – returns the packet to its previous chain and stops it from going forward

## The default table :

```
    INPUT – for incoming packets
    FORWARD – incoming packets to be forwarded
    OUTPUT – for outgoing packets
```

`└─ $ ▶ sudo iptables -A <chain> -i <interface> -p <protocol (tcp/udp) > -s <source> --dport <port no.>  -j <target>`

```
    – A – indicates that iptables are to be modified
    chain – name of chain such as INPUT, FORWARD or OUTPUT
    -i interface – network traffic whose traffic you want to control
    -p protocol – network protocol such as tcp/udp
    -s source – source ip address
    –dport – destination port number
    -j target – target name ACCEPT, DROP or RETURN. This will define the action to be taken in case a packet matches the rule.
```

---

## Allow traffic from localhost :

`└─ $ ▶ sudo iptables -A INPUT -i lo -j ACCEPT`

## Allow traffic to HTTP, HTTPS, SSH ports :

`└─ $ ▶ sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT`

`└─ $ ▶ sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT`

`└─ $ ▶ sudo iptables -A INPUT -p tcp --dport 443 -j ACCEPT`

## Allow traffic from specific IP address :

`└─ $ ▶ sudo iptables -A INPUT -s 54.34.44.22` -j ACCEPT`

## Disallow traffic from specific IP address :

`└─ $ ▶ sudo iptables -A INPUT -s 192.168.23.32 -j DROP`

## List iptables rules :

`└─ $ ▶ sudo iptables -L`

## Delete all iptables rules :

`└─ $ ▶ sudo iptables -F`

## Delete specific iptables rule :

`└─ $ ▶ sudo iptables -D INPUT 5`

(5 = rule number)

## iptables need to be redefined on reboot, so to make changes persistent :

**Look at the version of Linux at first** 

/etc/iptables.v4 

or 

/etc/iptablesv6

or

/etc/iptables.conf

`└─ $ ▶ sudo /sbin/iptables-save > /etc/iptables.conf`

## Even after restarting the computer the following example helps to reload the rules from the saved file.

`└─ $ ▶ sudo iptables-restore < /etc/iptables.conf`
