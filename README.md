# WebPack_learning
WebPack learning from https://www.codecademy.com/articles/react-setup-i

# Procedure
- WebPack Usage
That seems like an enormous amount of work to get a simple app up and running!
Perhaps it was, but that was in large part due to the fact that we slowly explained every step. Executing the steps by rote is much faster.
Here's a condensed version of how to get a React app up and running:
In the terminal, create a new directory. cd into that directory.
Type the following command-line scripts:
npm init
npm i -S {react,react-dom}
npm i -D babel-{core,loader} babel-preset-react
npm i -D webpack webpack-dev-server html-webpack-plugin
In your root directory, create a file named .babelrc. Write this inside:

In your root directory, create another file named webpack.config.js. Write (or copy) this inside:

In package.json, replace the scripts object with this:

Create a directory inside of your root directory named app, and another directory inside of app named app/components.
Create three new files: app/index.js, app/index.html, and app/components/App.js.
Copy the code from "Run a Local React App" into app/index.js and app/index.html. Make app/components/App.js the outermost component class of your new app.
In the terminal, type these two commands:



