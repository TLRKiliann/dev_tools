# HTTPS with React

1) Open up your root-folder and create a new folder called certification (or some other name of your choice).

2) Open up the certification and run this bit of code:

└─ $ ▶ openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365

(package.json)

```
  "scripts": {
    "start": "export HTTPS=true&&SSL_CRT_FILE=cert.pem&&SSL_KEY_FILE=key.pem react-scripts start",
    "build": "react-scripts build",
```

# HTTPS with Vite

└─ $ ▶ npm i vite-plugin-mkcert -D

(vite.config.js)

```
import { defineConfig } from 'vite'
import mkcert from 'vite-plugin-mkcert'

export default defineConfig({
  server: { https: true },
  plugins: [ mkcert() ]
})
```
