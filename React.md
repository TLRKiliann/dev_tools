
 /$$$$$$$                                  /$$    
| $$__  $$                                | $$    
| $$  \ $$  /$$$$$$   /$$$$$$   /$$$$$$$ /$$$$$$  
| $$$$$$$/ /$$__  $$ |____  $$ /$$_____/|_  $$_/  
| $$__  $$| $$$$$$$$  /$$$$$$$| $$        | $$    
| $$  \ $$| $$_____/ /$$__  $$| $$        | $$ /$$
| $$  | $$|  $$$$$$$|  $$$$$$$|  $$$$$$$  |  $$$$/
|__/  |__/ \_______/ \_______/ \_______/   \___/  
                                                  
                                                  
                                                  
                                                  


# INSTALL REACT


## !!! Never use npm install -g, use npm install --save-dev !!!

---

## Virtualenv

1. Create a directory UI-NodeReact (or any other name you want to start up with)

`└─ $ ▶ mkdir UI-NodeReact`

2. Create a virtual env for your project and let’s name it folder_name

`└─ $ ▶ virtualenv --no-site-packages name_folder`

2. Activate the virtual env

`└─ $ ▶ source folder_name/bin/activate`

`└─ $ ▶ cd folder_name`

`└─ $ ▶ pip install nodeenv`

`└─ $ ▶ nodeenv -p`

`└─ $ ▶ npm i -g create-react-app@3.0.1`

`└─ $ ▶ create-react-app react-app`


## Node.js

`└─ $ ▶ node -v`

`└─ $ ▶ sudo apt update`

`└─ $ ▶ sudo apt install nodejs`


## Npm

`└─ $ ▶ sudo apt install npm`

`└─ $ ▶ npm start`

`└─ $ ▶ npm install <package> --save-dev`

`└─ $ ▶ npm build`


## React

`└─ $ ▶ npx create-react-app name-app`

`└─ $ ▶ cd name-app`

`└─ $ ▶ ls`

`└─ $ ▶ npm install <package> --save-dev`


**Debugging & Testing**

- console.log()

- console of browser

- React Developer Tools (add-ons (google))

- npm run test


`└─ $ ▶ npm install @testing-library/react jest --save-dev`

App.test.js

```
import '@testing-library/jest-dom'
import {render, screen} from '@testing-library/react'
```

```
import {render, screen} from '@testing-library/react'

describe("SearchForm", () => {
   test("renders SearchForm", () => {
    render(<SearchForm/>);
    expect(screen.getByRole("heading", { name: /location search/i })
        ).toBeVisible();
        
    expect(screen.getByRole("textbox", { name: /choose an origin \(optional\)/i })
        ).toBeVisible();

    expect(screen.getByRole("textbox", { name: /choose a destination/i})
        ).toBeVisible();
        
    expect(screen.getByRole("button", { name: /search/i })
        ).toBeVisible();
  });
});
```

`└─ $ ▶ npm run test -- -t 'utils'`
