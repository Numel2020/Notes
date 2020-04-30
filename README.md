# Notes
## 1. Setting up a JsCongfig file in react-app
You can configure your application to support importing modules using absolute paths. This can be done by configuring a jsconfig.json or tsconfig.json file in the root of your project.

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
