### Tailwind CSS Projekt

## Requirements

Please make sure that you can use `npm`.<br>
You can install [node.js](https://nodejs.org/de) to get everything you need.

## Installation

1.  To install Tailwind open the Terminal and type `npm install -D tailwindcss`<br>
2.  To init the `tailwind.config.js` type `npx tailwindcss init`

## Configuration

1. Add the paths to all of your template files in your `tailwind.config.js` file.<br>

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./public/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

its important that you use the right path in the `content` section.

2. Add the `@tailwind` directives for each of Tailwind’s layers to your main CSS file.

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

its the css file in the src/css folder.

3. use youre `package.json` to configure the scripts section

```
{
  "scripts": {
    "watch": "npx tailwindcss -i ./src/css/style.css -o ./public/css/style.css --watch",
    "prod": "npx tailwindcss -i ./src/css/style.css -o ./public/css/style.css"
  },
  "devDependencies": {
    "tailwindcss": "^3.3.3"
  }
}
```

4. link the tailwind css in the html header:
   `<link href="/dist/output.css" rel="stylesheet">`

## Start creating a stunning website

you can now work with tailwind css. <br>
Just type `npm run watch`.

## Publish the website to ftp

you can publish the webiste by copying the `public` folder to a ftp dir.
