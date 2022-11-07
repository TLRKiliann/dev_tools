# Install

## Vite + React + TypeScript

└─ $ ▶ npm create vite@latest

> react

> TypeScript

└─ $ ▶ cd vite-project

└─ $ ▶ npm install

└─ $ ▶ npm run dev

## Sass

└─ $ ▶ npm install --save-dev sass

(index.html)
```
<style>
  @import url('./src/index.scss')
</style>
```

## Tailwind

https://tailwindcss.com/docs/guides/vite

└─ $ ▶ npm install -D tailwindcss postcss autoprefixer

└─ $ ▶ npx tailwindcss init -p

(tailwind.config.cjs)

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

(index.scss)

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

└─ $ ▶ npm run dev

(App.tsx)

```
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
```
