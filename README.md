### :zap: `Webpack 5 Boilerplate for JS apps.`
## Version 1.0.1

In development mode asset/inline style
In production mode asset/resource style
- added mini-css-extract-plugin
- added webpack.ProgressPlugin
- added loading fonts
- added eslint-webpack-plugin for development mode
- added folding resources to folders in the production mode
  - images
  - style
  - fonts
  - svg

## Version 1.0.0
## Includes

- 2 config for development and production mode
  - npm run start - for development
  - npm run build - for production
  
- sass, css, postcss
- import img and svg files
- import fonts

## To add 'tree shaking' option:
 - to webpack.config.js
```javascript
module: {
    rules: [
      {
        test: /\.(js|jsx)$/,
        exclude: /node_modules/,
        use: {
          loader: babel-loader,       
          side-effects: false,
          /* This configuration aids babel-preset-env to disable transpiling of import or export modules to commonJS */
          options: {
            presets: [
              [ 'es2015', { modules: false }]
            ]
          }
        }
      }
    ]
  },
```
- Use ES2015 module syntax (i.e. import and export).
```javascript
// ES2015(ES6) Sample of importing a specific dependency with tree shaking
import isArray from 'lodash/isArray'
```
