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
## 6. zsh-shell 
[make-an-alias(https://wpbeaches.com/make-an-alias-in-bash-or-zsh-shell-in-macos-with-terminal/)

