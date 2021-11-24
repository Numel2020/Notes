# Notes
## 1. Setting up a `JsCongfig.json` file in react-app
You can configure your application to support importing modules using absolute paths. This can be done by configuring a `jsconfig.json` or `tsconfig.json` file in the root of your project.

```javascript
{
  "compilerOptions": {
    "baseUrl": "./src"
  },
  "exclude": ["node_modules", "**/node_modules/*"]
}
```
Now that you've configured your project to support absolute imports, if you want to import a module located at src/components/Button.js, you can import the module like so:

```javascript
import Button from 'components/Button';
```
[jsconfig.json - What is jsconfig.json?](https://code.visualstudio.com/docs/languages/jsconfig)

## 2. Creating a new package.json file
To create a package.json file with values that you supply, use the npm init command.
1. On the command line, navigate to the root directory of your package.
```
cd /path/to/package
```
2. Run the following command:
  ```
  npm init
  ```
3. Answer the questions in the command line questionnaire.

## 3. Which node?
In the terminal type.
```
which node
```
Then you can see the path of your used node installation.

## 4. iteration on HTML Collections
In ES6, you could do something like `[...collection]`, or `Array.from(collection)`,
```
let someCollection = document.querySelectorAll(someSelector)
[...someCollection].forEach(someFn) 
//or
Array.from(collection).forEach(someFn)
```
## 5. hide Project tool window in phpStorm
Press cmd + 1
## 6. zsh-shell config
[1. Make-an-alias](https://wpbeaches.com/make-an-alias-in-bash-or-zsh-shell-in-macos-with-terminal/)
## 7. Promises
[What happens if you don't resolve or reject a promise?](https://stackoverflow.com/questions/36734900/what-happens-if-you-dont-resolve-or-reject-a-promise)

[Using mongoose promises with async/await](https://stackoverflow.com/questions/46457071/using-mongoose-promises-with-async-await)

[Intellij Idea warning - "Promise returned is ignored" with aysnc/await](https://stackoverflow.com/questions/41278900/intellij-idea-warning-promise-returned-is-ignored-with-aysnc-await)

## 8. API
[How to build node.js rest api with express and Mongo DB](https://medium.com/bb-tutorials-and-thoughts/how-to-build-nodejs-rest-api-with-express-and-mongodb-fa6e1610ee1b)

## 9. Mongoose
[Close a mongoose connection](https://stackoverflow.com/questions/8813838/properly-close-mongooses-connection-once-youre-done)

## 10. API and CRUD examples
[bbachi - nodejs-restapi-mongo - Public](https://github.com/bbachi/nodejs-restapi-mongo/blob/main/config/db.config.js)

[CodAffection - Node.js-Expess-MongoDB-CRUD - Public](https://github.com/CodAffection/Node.js-Expess-MongoDB-CRUD/blob/master/project/controllers/employeeController.js)

[iamshaunjp - node-crash-course - Public](https://github.com/iamshaunjp/node-crash-course/blob/lesson-12/app.js)

[trulymittal - Nodejs-REST-API - Public](https://github.com/trulymittal/Nodejs-REST-API/blob/master/Controllers/Product.Controller.js)

## 11. Express

[A Guide to Error Handling in Express.js](https://scoutapm.com/blog/express-error-handling)

## 12. Node
```
export NODE_ENV=production
echo $NODE_ENV
```

