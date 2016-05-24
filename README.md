ts-webpack
===========================

It's time consuming to combine all components together and make things work well.
This project template helps you create a whole new project that comes with
pre-installed typescript, webpack, babel settings together. Therefore, you can
just code from `entry.ts` without worring anything about babel settings,
webpack settings...

## Installation

    sudo npm install typescript -g
    sudo npm install typings -g
    sudo npm install webpack -g
    sudo npm install webpack-dev-server -g

    sudo npm link typescript
    npm install
    typings install

## Build

Run webpack to build the files

    webpack

Run webpack-dev-server:

    webpack-dev-server

## Guide

### Modify your webpack target entry name

    vim webpack.config.js

Change 

```js
module.exports = {
    'entry': {
        'myproj': ['./entry'],
    }
}
```

To whatever you want.


### Start Coding

Just start coding from `entry.ts` and `src/...` without worring anything!

### Get Your Type Definition Files

Sample commands:

    typings install dt~d3 --save --global
    typings install dt~jquery --save --global
    typings install dt~mocha --save --global

### ts-loader + babel-loader is too slow!?

You can simply change the `target` from `es6` to `es5` in `tsconfig.json` and
remove the `babel-loader` from `webpack.config.js`.

### Advanced babelrc Config File

.babelrc

```
{
    "presets": ["es2015", "es2015-native-modules"],
    "plugins": [
        "transform-runtime",
        [
        "transform-es2015-modules-commonjs", {
            "strict": false,
            "loose": true
        }],
        "babel-plugin-transform-object-assign"
    ]
}
```



## Author

Yo-An Lin (c9s)

