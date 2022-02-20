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

### Updating node

[n – Interactively Manage Your Node.js Versions](https://github.com/tj/n)

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

[Mongoose connection events with createConnection](https://stackoverflow.com/questions/24100119/mongoose-connection-events-with-createconnection/53192759)

[MongoError: not authorized on to execute command { find: "app_updates", filter: { key: "0.0.1-admins" }, limit: 1, batchSize: 1, singleBatch: true }](https://stackoverflow.com/questions/47130379/mongoerror-not-authorized-on-to-execute-command-find-app-updates-filter)

[User management in mongodb](https://scalegrid.io/blog/getting-started-with-user-management-in-mongodb/)

## 10. API and CRUD examples
[bbachi - nodejs-restapi-mongo - Public](https://github.com/bbachi/nodejs-restapi-mongo/blob/main/config/db.config.js)

[CodAffection - Node.js-Expess-MongoDB-CRUD - Public](https://github.com/CodAffection/Node.js-Expess-MongoDB-CRUD/blob/master/project/controllers/employeeController.js)

[iamshaunjp - node-crash-course - Public](https://github.com/iamshaunjp/node-crash-course/blob/lesson-12/app.js)

[trulymittal - Nodejs-REST-API - Public](https://github.com/trulymittal/Nodejs-REST-API/blob/master/Controllers/Product.Controller.js)

[Tariqu - REST_API_WITH_MYSQL - Public](https://github.com/Tariqu/REST_API_WITH_MYSQL)

[productioncoder - express-error-handling - Public](https://github.com/productioncoder/express-error-handling/blob/master/index.js)

[larswaechter - expressjs-api - Public](https://github.com/larswaechter/expressjs-api/blob/main/src/api/middleware/index.ts)

## 11. Express

[A Guide to Error Handling in Express.js](https://scoutapm.com/blog/express-error-handling)

[Create an Error handle for your express api](https://simonplend.com/how-to-create-an-error-handler-for-your-express-api/)

[Error Handling Patterns in Express.js](https://medium.com/@zachcaceres/error-handling-patterns-in-express-js-6ba0fc943c91)

[Express: scalable way to handle errors](https://dev.to/rajajaganathan/express-scalable-way-to-handle-errors-1kd6)

[How to create an error handler for your Express API](https://simonplend.com/how-to-create-an-error-handler-for-your-express-api/#next-steps)





### youtube

[Part 2 | Error Handling in express | 404 | RESTful API using #NodeJS and #MySQL](https://www.youtube.com/watch?v=WgxhIZ6gz3E)

[express-validator Node.js tutorial](https://www.youtube.com/watch?v=7i7xmwowwCY)

### validation

[Validating input in Express using express-validator](https://flaviocopes.com/express-validate-input/)

[Is it a good practice to use both Joi and express-validator?](https://stackoverflow.com/questions/63550183/is-it-a-good-practice-to-use-both-joi-and-express-validator)

[How to choose which validator to use: a comparison between Joi & express-validator](https://www.freecodecamp.org/news/how-to-choose-which-validator-to-use-a-comparison-between-joi-express-validator-ac0b910c1a8c/)

### Jest, test and mocks

[Sam-Meech-Ward - express_jest_and_mocks Public](https://github.com/Sam-Meech-Ward/express_jest_and_mocks/blob/master/app.js)

[rahmanfadhil - learn-supertest Public](https://github.com/rahmanfadhil/learn-supertest)

[TomDoesTech - Testing-Express-REST-API Public](https://github.com/TomDoesTech/Testing-Express-REST-API/blob/main/src/__tests__/user.test.ts)

[rahmanfadhil - learn-supertest Public](https://github.com/rahmanfadhil/learn-supertest/blob/master/server.test.js)

### mongodb-memory-server

[Integration with Test Runners](https://nodkz.github.io/mongodb-memory-server/docs/guides/integration-examples/test-runners)

### jest

[What's the difference between '.toMatchObject' and 'objectContaining'](https://stackoverflow.com/questions/45692456/whats-the-difference-between-tomatchobject-and-objectcontaining)


## 12. Node
To set node enviroment variable and check setting
```
export NODE_ENV=production
echo $NODE_ENV
```

You call list all variables for Macs available for your project directory with...
```
printenv
```
[Display NODE_ENV in command line](https://stackoverflow.com/questions/27935533/is-there-a-way-to-display-node-env-from-the-command-line)

[Node.js, the difference between development and production](https://nodejs.dev/learn/nodejs-the-difference-between-development-and-production)

[Node running in production](https://gist.github.com/leommoore/5763232)

## 13. Terminal
```
clear         - clear console window
mkdir         - create new directory
touch         - create a new file
```

## 14. Logging
[winston examples](https://coralogix.com/blog/complete-winston-logger-guide-with-hands-on-examples/)

[logging with winston](https://www.section.io/engineering-education/logging-with-winston/)

[Complete Winston Logger Guide With Hands-on Examples](https://coralogix.com/blog/complete-winston-logger-guide-with-hands-on-examples/)

[Creating custom tokens](https://findthedifficult.com/creating-custom-tokens-in-morgan-the-node-js-logger-middleware/)

[Node Express.js and Morgan logging](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/node-express-js-morgan-logging.htm)

[Morgan NPM Logger – The Beginner’s Guide](https://coralogix.com/blog/morgan-npm-logger-the-complete-guide/)

[node-js-logging-use-morgan-and-winston](https://stackoverflow.com/questions/27906551/node-js-logging-use-morgan-and-winston)

## 15. Api design and architecture
[The Web API Checklist -- 43 Things To Think About When Designing, Testing, and Releasing your API](https://mathieu.fenniak.net/the-api-checklist/)

[Folder Structure for API's - Beginner, Intermediate, and Advanced](https://www.youtube.com/watch?v=oNlMrpnUSFE)

[Server-Side Validation with API Descriptions](https://apisyouwonthate.com/blog/server-side-validation-with-api-descriptions)

[Best Practices for Designing a Pragmatic RESTful API](https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api)

[REST API Best Practices – REST Endpoint Design Examples](https://www.freecodecamp.org/news/rest-api-best-practices-rest-endpoint-design-examples/)

[REST: Good Practices for API Design](https://medium.com/hashmapinc/rest-good-practices-for-api-design-881439796dc9)

[Four REST API Versioning Strategies](https://www.xmatters.com/blog/blog-four-rest-api-versioning-strategies/)

### API responses
[api-requests and responses](https://docs.beeswax.com/docs/api-requests-and-responses)

### API errors
[REST API Error Codes 101](https://blog.restcase.com/rest-api-error-codes-101/)

## JWT Authentication

[6 Minute Overview of Implementing JWT Authentication](https://www.youtube.com/watch?v=1HHrkZ6h0Z0)

[Learn JWT in 10 Minutes with Express, Node, and Cookie Parser](https://www.youtube.com/watch?v=dX_LteE0NFM)

[JWT Authentication Tutorial - Node.js and React](https://www.youtube.com/watch?v=Yh5Lil03tpI&t=1039s)

[JWT Refresh Token | Node.js Tutorial](https://www.youtube.com/watch?v=jHQAfPFrTPo)

[JWT Authentication | Node JS and Express tutorials for Beginners](https://www.youtube.com/watch?v=favjC6EKFgw)

### Ben Awad - JWT series

[GraphQL JWT Authentication Implementation - part 1](https://www.youtube.com/watch?v=RUZB8tpyDbQ)

[GraphQL Refresh and Invalidate JWTs - part 2](https://www.youtube.com/watch?v=KkkdwK1VbLc)

### JWT - theory

[verify-a-jwt-token-string-containing-bearer-with-nodejs](https://stackoverflow.com/questions/39992774/verify-a-jwt-token-string-containing-bearer-with-nodejs/51963067)

[JWT.IO allows you to decode, verify and generate JWT](https://jwt.io/)

### refresh tokens

[Authentication With Refresh Tokens Implementation #benaward](https://www.youtube.com/watch?v=UA0AIkjI85c)

[Different Authentication Methods for Handling JWT Tokens](https://www.youtube.com/watch?v=wKkKFkeqFEU)

## API Keys

[Best practices for building secure API Keys](https://www.freecodecamp.org/news/best-practices-for-building-api-keys-97c26eabfea9)

## Roles
[Role Based API Authentication | Node Express MongoDB | Part 1](https://www.youtube.com/watch?v=QbgJgZY7vBM)

[Role Based API Authentication | Node Express MongoDB | Part 2](https://www.youtube.com/watch?v=VXzluXTBFF8)
