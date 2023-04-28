# Tailwind-CSS
 
 ##  Tailwind-CSS Documentation ('https://tailwindcss.com/docs/installation')

## Setup CLI + Prettier

## Setup CLI 

1. Open your terminal or command prompt and navigate to your project directory.

2. Install Node.js and npm (Node Package Manager) if you haven't already installed them on your system. You can download Node.js from https://nodejs.org/en/download/ and it will come with npm included.

3. Initialize a new npm project in your project directory by running the following command:

    ```
    npm init -y
    ```
4. Install Tailwind CSS
Install tailwindcss via npm, and create your tailwind.config.js file.
```
Terminal

npm install -D tailwindcss
npx tailwindcss init
```
5. Configure your template paths
Add the paths to all of your template files in your `tailwind.config.js` file.
```
tailwind.config.js

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

6. Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.
```
src/input.css

@tailwind base;
@tailwind components;
@tailwind utilities;
```
7. Start the Tailwind CLI build process
Run the CLI tool to scan your template files for classes and build your CSS.
```
Terminal

npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch


```
8. Start using Tailwind in your HTML
Add your compiled CSS file to the `<head>` and start using Tailwind’s utility classes to style your content.
```
src/index.html

<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

## Prettier Setup


<img src='https://tailwindcss.com/_next/static/media/prettier-banner.79c40690.jpg' width='70%' >

<br>


A [Prettier](https://prettier.io/) plugin for Tailwind CSS v3.0+ that automatically sorts classes based on [our recommended class order](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier#how-classes-are-sorted).

## Installation

To get started, just install `prettier-plugin-tailwindcss` as a dev-dependency:

```sh
npm install -D prettier prettier-plugin-tailwindcss
```

This plugin follows Prettier’s autoloading convention, so as long as you’ve got Prettier set up in your project, it’ll start working automatically as soon as it’s installed.

_Note that plugin autoloading is not supported when using certain package managers, such as pnpm or Yarn PnP. In this case you may need to add the plugin to your Prettier config explicitly:_

```js
// prettier.config.js
module.exports = {
  plugins: [require('prettier-plugin-tailwindcss')],
}
```


