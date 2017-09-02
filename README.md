# WebPack_learning
WebPack learning from https://www.codecademy.com/articles/react-setup-i

# Procedure
Type the following command-line scripts:
- npm init
- npm i -S {react,react-dom}
- npm i -D babel-{core,loader} babel-preset-react
- npm i -D webpack webpack-dev-server html-webpack-plugin
In your root directory, create a file named .babelrc. Write this inside:
`{
  "presets": ["react"]
}
`
In your root directory, create another file named webpack.config.js. Write (or copy) this inside:

In package.json, replace the scripts object with this:

Create a directory inside of your root directory named app, and another directory inside of app named app/components.
Create three new files: app/index.js, app/index.html, and app/components/App.js.
Copy the code from "Run a Local React App" into app/index.js and app/index.html. Make app/components/App.js the outermost component class of your new app.
In the terminal, type these two commands:



