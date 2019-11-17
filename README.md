### BABEL_CHEAT_SHEET

#### babel-cli

- purpose: `simple way to compile files with Babel from the command line.`
- installation: `$ npm install --global babel-cli`
- installation locally: `$ npm install --save-dev babel-cli`
- write on a file `$ babel example.js --out-file compiled.js`
- write on a file `$ babel example.js -o compiled.js`
- compile in a new directory `$ babel src --out-dir lib`

#### babel-register
- purpose: `allow you to run Babel just by requiring files`
- installation: `$ npm install --save-dev babel-register`
- usage:
```javascript
// file is babel-register.js
require("babel-register");
require("./index.js");
// command to run node babel-register.js
```

#### babel-node
- purpose: `the easiest way to integrate running scripts with babel`
- installation: `$ npm install --save-dev babel-cli`
```JSON
{
    "scripts": {
      "script-name": "node script.js",
      "script-name": "babel-node script.js"
    }
}
```

#### babel-core
- purpose: `if you need to use babel programmatically`
- installation: `$ npm install babel-core`
- usage
```javascript
// transforming code
babel.transform("code();", options);
// => { code, map, ast }
```
```javascript
// transforming file async
babel.transformFile("filename.js", options, function(err, result) {
  result; // => { code, map, ast }
});
```
```javascript
// transform file sync
babel.transformFileSync("filename.js", options);
// => { code, map, ast }
```
```javascript
// if you already have the AST
babel.transformFromAst(ast, code, options);
// => { code, map, ast }
```

#### .babelrc
- purpose `configuration file for babel`

#### babe-preset-2015
- purpose: `compile es6 to es5`
- installation: `$ npm install --save-dev babel-preset-es2015`
- usage:
```JSON
{
  "presets": [
    "es2015"
  ],
  "plugins": []
}
```

#### babel-preset-react
- purpose: `Setting up React is just as easy`
- installation: `$ npm install --save-dev babel-preset-react`
- usage:
```JSON
{
  "presets": [
    "es2015",
    "react"
  ],
  "plugins": []
}
```

#### babel-preset-stage-x
- purpose: using babel proposals in the different stages
- installation: `$ npm install --save-dev babel-preset-stage-2`
- usage:
```JSON
{
  "presets": [
    "es2015",
    "react",
    "stage-2"
  ],
  "plugins": []
}
```
#### babel-polyfill
- purpose: `a polyfill is a piece of code that replicates a native api that does not exist in the current runtime`
- installtion: `$ npm install --save babel-polyfill`
- usage; simply `import "babel-polyfill";` in every file that needs it

#### babel-runtime
- purpose: `in order to implement details of ECMAScript specs`
- installtion; `$ npm install --save babel-runtime`
