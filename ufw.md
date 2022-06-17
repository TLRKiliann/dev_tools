# UFW

## Status

`└─ $ ▶ sudo ufw status`

**Verbose**

└─ $ ▶ sudo ufw status verbose`

## Activate

└─ $ ▶ sudo ufw enable`

## Deactivate

└─ $ ▶ sudo ufw disable`

## Reload

└─ $ ▶ sudo ufw reload`

# Reset

└─ $ ▶ sudo ufw reset`

## Allow traffic whith HTTPS

└─ $ ▶ sudo ufw allow 443`

└─ $ ▶ sudo ufw allow tcp`

└─ $ ▶ sudo ufw allow 443/tcp`

## Allow connection http with 176.234...

sudo ufw allow http from 176.234.111.232

## Deny

└─ $ ▶ sudo ufw deny 22`

└─ $ ▶ sudo ufw deny ssh`

└─ $ ▶ sudo ufw deny 22/ssh`

## Deny ssh from addr 110.187...

└─ $ ▶ sudo ufw deny 22 from 110.187.234.22`
