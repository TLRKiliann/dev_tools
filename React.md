     ..      ...                                           s    
  :~"8888x :"%888x                                        :8    
 8    8888Xf  8888>                                      .88    
X88x. ?8888k  8888X       .u          u           .     :888ooo 
'8888L'8888X  '%88X    ud8888.     us888u.   .udR88N  -*8888888 
 "888X 8888X:xnHH(`` :888'8888. .@88 "8888" <888'888k   8888    
   ?8~ 8888X X8888   d888 '88%" 9888  9888  9888 'Y"    8888    
 -~`   8888> X8888   8888.+"    9888  9888  9888        8888    
 :H8x  8888  X8888   8888L      9888  9888  9888       .8888Lu= 
 8888> 888~  X8888   '8888c. .+ 9888  9888  ?8888u../  ^%888*   
 48"` '8*~   `8888!`  "88888%   "888*""888"  "8888P'     'Y"    
  ^-==""      `""       "YP'     ^Y"   ^Y'     "P'              
                                                                
                                                                
                                                                
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
