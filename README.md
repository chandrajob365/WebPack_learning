# WebPack_learning
WebPack learning from https://www.codecademy.com/articles/react-setup-i
.Its a five part series

# Procedure
Type the following command-line scripts:
- npm init
- npm i -S {react,react-dom}
- npm i -D babel-{core,loader} babel-preset-react
- npm i -D webpack webpack-dev-server html-webpack-plugin
- In your root directory, create a file named .babelrc. Write this inside:
```json
{
  "presets": ["react"]
}
```

- In your root directory, create another file named webpack.config.js. Write (or copy) this inside:
```
const HTMLWebpackPlugin = require('html-webpack-plugin')
const HTMLWebpackPluginConfig = new HTMLWebpackPlugin({
  template: __dirname + '/app/index.html',
  filename: 'index.html',
  inject: 'body'
})

module.exports = {
  entry: __dirname + '/app/index.js',
  module: {
    loaders: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        loader: 'babel-loader'
      }
    ]
  },
  output: {
    filename: 'transformed.js',
    path: __dirname + '/build'
  },
  plugins: [HTMLWebpackPluginConfig]
}
```
- In package.json, replace the scripts object with this:
```json
{
 "scripts": {
    "build": "webpack",
    "start": "webpack-dev-server"
  }
};
```
- Create a directory inside of your root directory named app, and another directory inside of app named app/components.
- Create three new files: app/index.js, app/index.html, and app/components/App.js.
- Copy the code from "Run a Local React App" into app/index.js and app/index.html. Make app/components/App.js the outermost     component class of your new app.
- In the terminal, type these two commands: `npm run build` and `npm run start`



