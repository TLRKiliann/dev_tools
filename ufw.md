# UFW (commands)

## Status

`└─ $ ▶ sudo ufw status`

Verify if rsyslog is enable :

`└─ $ ▶ service rsyslog status`

**Verbose**

`└─ $ ▶ sudo ufw status verbose`


## App List

`└─ $ ▶ sudo ufw app list`

`└─ $ ▶ sudo ufw app info "Apache Full"`


## Logging

`└─ $ ▶ sudo ufw logging on`

`└─ $ ▶ sudo ufw logging low`

`└─ $ ▶ sudo ufw logging medium`

To follow the log in real time :

`└─ $ ▶ tail -f /var/log/ufw.log`


## Activate

`└─ $ ▶ sudo ufw enable`


## Deactivate

`└─ $ ▶ sudo ufw disable`


## Reload

`└─ $ ▶ sudo ufw reload`


## Reset

`└─ $ ▶ sudo ufw reset`


## Rules

List all the rules :

`└─ $ ▶ sudo ufw status numbered`

See <Delete> to know how manage rules.


## Insert NUM RULE

`└─ $ ▶ sudo ufw insert 1 deny in from 12.34.56.78 to any port 25 proto tcp`


## Allow traffic whith HTTPS

`└─ $ ▶ sudo ufw allow 443`

`└─ $ ▶ sudo ufw allow 443/tcp`

**Allow incoming connection :**

`└─ $ ▶ sudo ufw allow in http from 176.234.111.232`


## Deny

`└─ $ ▶ sudo ufw deny 22`

`└─ $ ▶ sudo ufw deny ssh`

`└─ $ ▶ sudo ufw deny 22/ssh`

Block an IP address :

`└─ $ ▶ sudo ufw deny from 203.0.113.100`

Block only port 22 from 110.187... :

`└─ $ ▶ sudo ufw deny 22 from 110.187.234.22`


## Reject

`└─ $ ▶ sudo ufw reject out smtp `

**With comment**

`└─ $ ▶ sudo ufw reject telnet comment 'telnet is unencrypted'`


## Delete

`└─ $ ▶ sudo ufw delete 80/tcp`

Delete rule number 3 :

`└─ $ ▶ sudo ufw delete 3`


## With log

To allow and log all new ssh connections :

`└─ $ ▶ sudo ufw allow log 22/tcp`


## Some examples

Deny access to udp port 514 from host 1.2.3.4:

`└─ $ ▶ sudo ufw deny proto udp from 1.2.3.4 to any port 514`

