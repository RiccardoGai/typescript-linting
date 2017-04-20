# Typescript Linting
Typescript linting for Snagajob Angular 2 Projects.

Linting?? sounds like extra work... TRUE, but we strive for re-usable components right? Besides have you ever worked on old code and got frustrated by how unreadbale it was? Let's not do that to each other. We can start with linting.

Linting will go through .ts files and flag code that breaks our standards. 

For a link to our standards check out our [Javascript Style Guide.](https://github.com/Snagajob/javascript)

## Dependencies
In your project's package.json ensure you have the following dependencies. We build on air bnb's linting config, and tweak it a little for our use.

+ [tslint](https://www.npmjs.com/package/tslint)
+ [tslint-config-airbnb](https://www.npmjs.com/package/tslint-config-airbnb)

If you don't have npm, [install it with homebrew.](http://blog.teamtreehouse.com/install-node-js-npm-mac)

If you do, run the command below to save the packages right to your package.json.

```
npm install --save-dev --save-exact tslint@latest tslint-config-airbnb@latest
```

## tslint.json
Grab the tslint.json file from this repo and add it to the root (lowest directory) of your project.

## Use Linting in Visual Studio Code
Add tslint to your Visual Studio Code extensions:

1. Open Visual Studio Code and go to Extensions
2. Search 'tslint' (no quotes)
3. Install and restart Visual Studio Code

Now the extension will be using our tslint.json config file to flag code in red.

## Use Linting with NPM
Use the following command to run linting.

```
npm run tslint "src/**/*.ts"
```

This command takes a directory where all your .ts files reside, usually src/ or app/. **/*.ts acts as a wild card to find all the .ts files under that directory. You can be more specific if you'd like, and specify a file to lint.

## Set up a Script in package.json
For those of you who don't want to run a long command every time you need to lint your entire project, you can add a lint script to your package.json. 

Under the 'scripts' property, add the following commands.
```
*package.json

"scripts": {
  "lint": "npm run tslint 'src/**/*.ts\'",
  "tslint": "tslint",
}
```

Now in your console you can run 'npm lint' to get a console print out of all the lint errors in your project.
```
npm lint
```

## Include Linting in your Build process.
Now that you included linting in your packge.json scripts, add that script to your build process.

This is the best way to ensure all code getting built meets our standard.