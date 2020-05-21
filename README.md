# Svelte-Webpack-TailwindCSS-Typescript-Template

A starter template for svelte using webpack and tailwind css adn typescript. Webpack is usefull because it has a dev-server plugin that lets you proxy your apps request while you develope it with a local rest api.

by default I have set the dev-server to proxy any request the app makes starting with "/api" through "http://localhost:3000". This behavior can be changes in webpack.config.js.

tailwind outputs classes to src/CSS/tailwind.css and is configured to use the built in class purging to remove unused classes at build (the tailwind doc says it is faster than purgecss ¯\\\_(ツ)\_/¯). build output files are minified.

## Configuration

There are a number of dependencies that I have included because I have used them in many projects and found them useful.

- [tailwindcss-bg-alpha](https://github.com/adfdev/tailwindcss-bg-alpha)
- [tailwindcss-dark-mode](https://github.com/ChanceArthur/tailwindcss-dark-mode)
- [svelte-media](https://github.com/cibernox/svelte-media)
- [autoprefixer](https://github.com/postcss/autoprefixer)

svelte-media has a store that exposes media queries for you to use in your code. the darkMode store has turnOn() and turnOff() functions to turn on and off the dark mode, which you can specify in your css with the dark: selector ie. dark:bg-gray-900

I have set up a color palette that conforms to the material design [color palette](https://material.io/design/color/the-color-system.html#tools-for-picking-colors) but I have also included a dark-gray color for use with dark mode.

## Getting Started

-clone the repo
-install dependencies

```
npm install
```

-run dev server

```
npm run start
```

-run build

```
npm run build
```

-deploy the public directory
