# Install babel

npm init interactively creates a package.json file for your project.
The -D switch to the npm install adds the packages to the dependency list in the package.json.
babel-preset-env is the library for doing the ES6+ to ES5 transpilation.

```
$ npm init
$ npm install babel-cli -D
$ npm install babel-preset-env -D
```

# Create .babelrc

Create a .babelrc file with the following contents to transpile ES6+ to ES5:

```
{
  "presets": ["env"]
}
```

# Add the babel build script to the package.json file

Add the following to the scripts object in package.json.  Don't forget a comma after any other properties.

```
"build": "babel src -d lib"
```

This will run babel on any .js files in the src directory and put the ES5 .js files in the lib directory.

# Run the build script

```
$ npm run build
```
