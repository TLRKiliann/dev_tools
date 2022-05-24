                                             
                                                                                                  
                                                                                                  
            RRRRRRRRRRRRRRRRR                                                                   tttt          
            R::::::::::::::::R                                                               ttt:::t          
            R::::::RRRRRR:::::R                                                              t:::::t          
            RR:::::R     R:::::R                                                             t:::::t          
              R::::R     R:::::R    eeeeeeeeeeee    aaaaaaaaaaaaa      ccccccccccccccccttttttt:::::ttttttt    
              R::::R     R:::::R  ee::::::::::::ee  a::::::::::::a   cc:::::::::::::::ct:::::::::::::::::t    
              R::::RRRRRR:::::R  e::::::eeeee:::::eeaaaaaaaaa:::::a c:::::::::::::::::ct:::::::::::::::::t    
              R:::::::::::::RR  e::::::e     e:::::e         a::::ac:::::::cccccc:::::ctttttt:::::::tttttt    
              R::::RRRRRR:::::R e:::::::eeeee::::::e  aaaaaaa:::::ac::::::c     ccccccc      t:::::t          
              R::::R     R:::::Re:::::::::::::::::e aa::::::::::::ac:::::c                   t:::::t          
              R::::R     R:::::Re::::::eeeeeeeeeee a::::aaaa::::::ac:::::c                   t:::::t          
              R::::R     R:::::Re:::::::e         a::::a    a:::::ac::::::c     ccccccc      t:::::t    tttttt
            RR:::::R     R:::::Re::::::::e        a::::a    a:::::ac:::::::cccccc:::::c      t::::::tttt:::::t
            R::::::R     R:::::R e::::::::eeeeeeeea:::::aaaa::::::a c:::::::::::::::::c      tt::::::::::::::t
            R::::::R     R:::::R  ee:::::::::::::e a::::::::::aa:::a cc:::::::::::::::c        tt:::::::::::tt
            RRRRRRRR     RRRRRRR    eeeeeeeeeeeeee  aaaaaaaaaa  aaaa   cccccccccccccccc          ttttttttttt  
                                                                                                  
                                                                                                  
                                                                                                  
# Install REACT


## !!! Never use npm install -g !!! => use npm install --save-dev !
## use `npm audit fix --force` with precautions !

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


## Debugging & Testing

**You can use :**

- console.log()

- console of browser

- React Developer Tools (add-ons (google or firefox))

**With @testing-library/react & Jest**

Install testing lib & jest

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

`└─ $ ▶ npm run test`

or

`└─ $ ▶ npm run test -- -t 'utils'`
