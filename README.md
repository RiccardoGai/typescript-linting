# Typescript Linting
Set up Typescript linting for Snagajob Angular 2 Projects.

Linting?? sound like extra work... TRUE, but we strive for re-usable components right? Besides have you ever worked on old code and got frustrated by how unreadbale it was? Let's not do that to each other. We can start with linting.

Linting will go through .ts files and flag code that breaks our standards. 

## Dependencies
In your project's package.json ensure you have the following dependencies.

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

This command takes the directory of where all your .ts files reside. Usually src/ or app/ then **/*ts act as wild cards and find all the .ts files to lint. You can be more specific if you'd like, and specify a file to lint.

## Set up a Script in package.json
