# jQuery

## With React or Vite

`└─ $ ▶ pnpm install --save-dev jquery`

App.js

`import $ from "jquery"`

## CDN

**It's preferable to use jQuery module with React or Vite**

`<script>https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js</script>`

## Code example

```
import React, { useState } from 'react'
import reactLogo from './assets/react.svg'
import $ from 'jquery'
//window.$ = $;
import './App.css'

const App: React.FC = () => {
  const [count, setCount] = useState(0)

  $(function() {
    $(".button").click(function() {
      $("p").show();
    });
    $(".button--hide").click(function() {
      $("p").hide();
    });
  });

  $(function() {
    $("p.intro").css("cursor", "pointer")
    $("p.intro").click(function() {
      $("p.intro").css("color", "yellow")
    });
  });

  $(function() {
    $("button.test").click(function() {
      $("p.test").hide()
    });
  });

  $(function() {
    $("button.fade-in").click(function() {
      $("#paragraph").fadeIn("5000", function() {
        console.log("fadein complete")
      });
    });
    $("button.fade-out").click(function() {
      $("#paragraph").fadeOut("5000", function() {
        console.log("fadeout complete")
      });
    });
  });

  $(function() {
    $("#slide--down").click(function() {
      $("#paragraph").slideDown("2000", "linear");
    });
    $("#slide--up").click(function() {
      $("#paragraph").slideUp("2000", "linear");
    });
    $("#slide--toggle").click(function() {
      $("#paragraph").slideToggle("slow", function() {
        let newText = $('p');
        newText.append("<i>New TEXT append HERE !</i>");
        $("#paragraph").html(newText);
      });
    });
  });

  $(function() {
    $("button.animation").click(function() {
      $("p.animation").animate({fontSize:"40px", margin:"auto"}, 3000);
    });
  });

  $(function() {
    $("button.animation2").click(function() {
      $("p.animation2").animate({marginLeft:"700px"}, 3000);
    });
  });

  $(function() {
    $("#append").click(function() {
      $(".append--p:first").append("--Append text is to cool!--");
    });
    $("#prepend").click(function() {
      $(".prepend--p:last").prepend("--Prepend text is to easy!--");
    });
  });

  return (
    <div className="App">
      <div>
        <a href="https://vitejs.dev" target="_blank">
          <img src="/vite.svg" className="logo" alt="Vite logo" />
        </a>
        <a href="https://reactjs.org" target="_blank">
          <img src={reactLogo} className="logo react" alt="React logo" />
        </a>
      </div>
      <h1>Vite + React</h1>
      <div className="card">

        <p className="animation">
          Animate with jQuery !!!
        </p>
        <button className="animation">
          Animate !
        </button>

        <p className="animation2">
          Animate 2 with jQuery !!!
        </p>
        <button className="animation2">
          Animate 2 !
        </button>

        <div>
          <button id="append">Append text</button>
          <button id="prepend">Prepend text</button>

          <p className="append--p prepend--p">
            1 - My superLorem ipsum dolor sit amet, consectetur adipiscing elit
          </p>
          <p className="append--p prepend--p">
            2 - My superLorem ipsum dolor sit amet, consectetur adipiscing elit
          </p>
          <p className="append--p prepend--p">
            3 - My superLorem ipsum dolor sit amet, consectetur adipiscing elit
          </p>

          <button id="slide--down">slide dow</button>
          <button id="slide--up">slide up</button>
          <button id="slide--toggle">slide toggle</button>

          <button className="fade-in">fade-in</button>
          <button className="fade-out">fade-out</button>

          <p id="paragraph">
            My superLorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut 
            enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi 
            ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit 
            in voluptate velit esse cillum dolore eu fugiat nulla pariatur. 
            Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia 
            deserunt mollit anim id est laborum.
          </p>
        </div>

        <p className="test">
          My test jquery
        </p>
        <button className="test">
          Click to Hide !
        </button>

        <button onClick={() => setCount((count) => count + 1)}>
          count is {count}
        </button>

        <button className="button">
          Show paragraph Tag !
        </button>

        <button className="button--hide">
          Hide paragraph Tag !
        </button>

        <p className="intro">
          Edit <code>src/App.tsx</code> and save to test HMR
        </p>
      </div>
      <p className="read-the-docs">
        Click on the Vite and React logos to learn more
      </p>
    </div>
  )
}

export default App
```
