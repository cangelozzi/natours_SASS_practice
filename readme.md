
# NATOURS practicing SASS 

## For Development environment
```javascript
npm run start
```

### Facts
The project goal was to apply advanced CSS3 properties using SASS extension language, including Block, Element, Modifier methodology (commonly referred to as BEM). 
https://gist.github.com/rveitch/84cea9650092119527bc

### package.json
Great importance is given to scripts:
{
  "name": "natours",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",

    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",

    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },
  "author": "Camillo Angelozzi",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^8.6.0",
    "concat": "^1.0.3",
    "node-sass": "^4.9.0",
    "npm-run-all": "^4.1.3",
    "postcss-cli": "^5.0.0"
  }
}

