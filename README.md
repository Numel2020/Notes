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

## 9. MongoDB
[How To Design a Document Schema in MongoDB](https://www.digitalocean.com/community/tutorials/how-to-design-a-document-schema-in-mongodb)

[Manage Deployments with the Atlas Administration API](https://www.mongodb.com/docs/atlas/api/atlas-admin-api/)

[MongoDB Atlas Administration API (1.0)](https://www.mongodb.com/docs/atlas/reference/api-resources-spec/)



```javascript
// to embed a document
const Competitor = require("./competitor");

competitor: new Schema( Competitor.schema)

// to reference a document
 competitor: {
        type: mongoose.Schema.Types.ObjectId,
        ref: "Competitor"
    },
```

[How to use indexes in Mongodb](https://www.digitalocean.com/community/tutorials/how-to-use-indexes-in-mongodb)

[mongoose duplicates with the schema key unique](https://stackoverflow.com/questions/9024176/mongoose-duplicates-with-the-schema-key-unique)

How to to manually create the index on the database to ensure that only one entry can be created.

```mongodb

bodybuilding> db.betausers.createIndex({"name":1},{"unique":true})

```


## 9. Mongoose
[Close a mongoose connection](https://stackoverflow.com/questions/8813838/properly-close-mongooses-connection-once-youre-done)

[Mongoose connection events with createConnection](https://stackoverflow.com/questions/24100119/mongoose-connection-events-with-createconnection/53192759)

[MongoError: not authorized on to execute command { find: "app_updates", filter: { key: "0.0.1-admins" }, limit: 1, batchSize: 1, singleBatch: true }](https://stackoverflow.com/questions/47130379/mongoerror-not-authorized-on-to-execute-command-find-app-updates-filter)

[User management in mongodb](https://scalegrid.io/blog/getting-started-with-user-management-in-mongodb/)

[Using mongorestore for Restoring MongoDB Backups](https://www.bmc.com/blogs/mongodb-mongorestore/)

[How To Use mongodump for MongoDB Backups](https://www.bmc.com/blogs/mongodb-mongodump/)

## 10. API and CRUD examples
[bbachi - nodejs-restapi-mongo - Public](https://github.com/bbachi/nodejs-restapi-mongo/blob/main/config/db.config.js)

[CodAffection - Node.js-Expess-MongoDB-CRUD - Public](https://github.com/CodAffection/Node.js-Expess-MongoDB-CRUD/blob/master/project/controllers/employeeController.js)

[iamshaunjp - node-crash-course - Public](https://github.com/iamshaunjp/node-crash-course/blob/lesson-12/app.js)

[trulymittal - Nodejs-REST-API - Public](https://github.com/trulymittal/Nodejs-REST-API/blob/master/Controllers/Product.Controller.js)

[Tariqu - REST_API_WITH_MYSQL - Public](https://github.com/Tariqu/REST_API_WITH_MYSQL)

[productioncoder - express-error-handling - Public](https://github.com/productioncoder/express-error-handling/blob/master/index.js)

[larswaechter - expressjs-api - Public](https://github.com/larswaechter/expressjs-api/blob/main/src/api/middleware/index.ts)

## 10.9. API Documentation examples
[WSO2 API Manager](https://apim.docs.wso2.com/en/4.0.0/)

[FusionAuth APIs](https://fusionauth.io/docs/v1/tech/apis/api-keys)

[Posit Connect](https://docs.posit.co/connect/user/api-keys/)

[Knowledge Base](https://support.flatfile.com/hc/en-us/articles/4406299638932-How-can-I-create-API-Keys-?campaignid=15403546517&adgroupid=129024558703&network=g&creative=565754187322&keyword=&matchtype=&placement=&targetid=dsa-19959388920&target=&device=c&device_model=&GA_loc_physical_ms=9046356&adposition=&GA_loc_interest_ms=&feed_item_id=&random=16761473912006351829&utm_term=&utm_campaign=Dynamic+Search+Ads&utm_source=adwords&utm_medium=ppc&hsa_acc=3330093901&hsa_cam=15403546517&hsa_grp=129024558703&hsa_ad=565754187322&hsa_src=g&hsa_tgt=dsa-19959388920&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwu_mSBhAYEiwA5BBmf7xTQNzbLuFPm-qwjq-IWF6dfhJ7tYkXZOnBYePXV-6Ns4G3EgYYyxoCkNoQAvD_BwE)

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

### Api examples

[TomDoesTech REST-API-Tutorial-Updated](https://github.com/TomDoesTech/REST-API-Tutorial-Updated)
[TomDoesTech Auth-api-tutorial - Public](https://github.com/TomDoesTech/auth-api-tutorial)

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

[benawad - graphql-express-template](https://github.com/benawad/graphql-express-template)

[benawad - jwt-auth-example](https://github.com/benawad/jwt-auth-example/blob/master/server/src/auth.ts)

### gitdagray
[Express JS Tutorial - JWT Protected Routes](https://github.com/gitdagray/express_jwt)

### JWT - theory

[verify-a-jwt-token-string-containing-bearer-with-nodejs](https://stackoverflow.com/questions/39992774/verify-a-jwt-token-string-containing-bearer-with-nodejs/51963067)

[JWT.IO allows you to decode, verify and generate JWT](https://jwt.io/)

### refresh tokens

[Authentication With Refresh Tokens Implementation #benaward](https://www.youtube.com/watch?v=UA0AIkjI85c)

[Different Authentication Methods for Handling JWT Tokens](https://www.youtube.com/watch?v=wKkKFkeqFEU)

## API Keys

[How the Heck Do API Keys Work?](https://www.youtube.com/watch?v=cF_MCAmuoI4)

[How to api](https://github.com/prof3ssorSt3v3/how-to-api)

[Generating Your Own API Tokens for a Node + Express API - 1,000 Subscribers 🎉🎉](https://www.youtube.com/watch?v=fmGBz2CAEeM&t=578s)

[Best practices for building secure API Keys](https://www.freecodecamp.org/news/best-practices-for-building-api-keys-97c26eabfea9)


## Roles
[Role Based API Authentication | Node Express MongoDB | Part 1](https://www.youtube.com/watch?v=QbgJgZY7vBM)

[Role Based API Authentication | Node Express MongoDB | Part 2](https://www.youtube.com/watch?v=VXzluXTBFF8)

[Implementing Role-Based Access Control in a Node.js application](https://soshace.com/implementing-role-based-access-control-in-a-node-js-application/)

[What is the best way to implement roles and permission in Express REST Api](https://stackoverflow.com/questions/38893178/what-is-the-best-way-to-implement-roles-and-permission-in-express-rest-api)

[Node.js - Role Based Authorization Tutorial with Example API](https://jasonwatmore.com/post/2018/11/28/nodejs-role-based-authorization-tutorial-with-example-api)

[How to implement dynamic Role-based Access Control (RBAC) in Express JS REST API.](https://dev.to/richienabuk/how-to-implement-dynamic-role-based-access-control-rbac-in-express-js-rest-api-54fe)

### seed a mongo database
[Igbo API](https://github.com/ijemmao/igbo_api)

[Seeding a MongoDB Database with NodeJS and Express for the Igbo Dictionary API](https://www.youtube.com/watch?v=fBQe3ZRPVdI)

## Google Drive api
[How to upload image to Google Drive using Node js](https://www.youtube.com/watch?v=-YZRkIbNWY0&t=18s)

[Upload Image to Google drive with Node Js](https://www.daimto.com/upload-image-to-google-drive-with-node-js)

[Google-auth-library documentation](https://googleapis.dev/nodejs/google-auth-library/5.10.1/classes/JWT.html#info)

[What keyFile key does google.auth.GoogleAuth() need?](https://stackoverflow.com/questions/60574191/what-keyfile-key-does-google-auth-googleauth-need)

[Where do I get Google Drive Folder, Shared Drive, or File ID?](https://robindirksen.com/blog/where-do-i-get-google-drive-folder-id)

### Key concerns
[Error 1e08010c decoder routines unsupported with google auth library](https://stackoverflow.com/questions/74131595/error-error1e08010cdecoder-routinesunsupported-with-google-auth-library)

[Adding rsa key in device variables](https://forums.balena.io/t/adding-rsa-key-in-device-variables/362396/9)

[What are the different formats of private key and certificates](https://www.googlecloudcommunity.com/gc/Apigee/What-are-the-different-formats-of-private-key-and-certificates/m-p/55180)

[Stop downloading google cloud service account keys](https://jryancanty.medium.com/stop-downloading-google-cloud-service-account-keys-1811d44a97d9)

[Using private key in a env file](https://stackoverflow.com/questions/55459528/using-private-key-in-a-env-file)


## GPG
To run:
```
$ gpg --full-gen-key
```
List keys that you have:
```
$ gpg --list-keys
```

[Basic File Encryption with GPG key pairs!](https://www.youtube.com/watch?v=DMGIlj7u7Eo)

[Install GPG on Mac without GPG Tools](https://mikeross.xyz/gpg-without-gpgtools-on-mac/)

[Quick'n easy gpg cheatsheet](http://irtfweb.ifa.hawaii.edu/~lockhart/gpg/)

[Gpg-xxxxxxxx-skipped-public-key-not-found](https://stackoverflow.com/questions/57251111/gpg-xxxxxxxx-skipped-public-key-not-found)

[There is no assurance this key belongs to the named user](https://stackoverflow.com/questions/33361068/gnupg-there-is-no-assurance-this-key-belongs-to-the-named-user)

[How to make auto trust gpg public-key](https://stackoverflow.com/questions/13116457/how-to-make-auto-trust-gpg-public-key)

## Dropbox API

[Using Dropbox as a headless CMS for a static blog](https://www.codemzy.com/blog/dropbox-headless-cms)

[How to get long lived access (refresh) tokens for Dropbox developer apps](https://www.codemzy.com/blog/dropbox-long-lived-access-refresh-token)

[Dropbox Node SDK](https://dropbox.github.io/dropbox-sdk-js/global.html#FilesUploadArg__anchor)

[Dropbox/dropbox-sdk-js](https://github.com/dropbox/dropbox-sdk-js/blob/main/examples/javascript/simple-backend/code_flow_example.js#L38)

## Github Workflows

[Why The Action Cannot Access Secrets?](https://stackoverflow.com/questions/61308519/why-the-action-cannot-access-secrets/61313152#61313152)

[How can I install Mongodb database tools on Github actions?](https://www.mongodb.com/community/forums/t/how-can-i-install-mongodb-database-tools-on-github-actions/208006)

[How to Build CI/CD Pipelines for MongoDB Realm Apps Using GitHub Actions](https://www.mongodb.com/developer/products/realm/build-ci-cd-pipelines-realm-apps-github-actions/)

[mongodb-developer
/
realm-demos
Public](https://github.com/mongodb-developer/realm-demos/blob/main/.github/workflows/build.yml)

[GitHub Actions — Exporting Multi-Line / One-Line Value Environment Variable](https://medium.com/@ibraheemabukaff/github-actions-exporting-multi-line-one-line-value-environment-variable-5bb86d01e866)

## KEYS
In javascript you can use a key like this
```
const key ="-----BEGIN PRIVATE KEY-----\nMIIEu...rzI\n-----END PRIVATE KEY-----\n".split(String.raw`\n`).join("\n");
```

## VITE
[How to Use Winston in Vite](https://dev.to/kjk93/how-to-use-winston-in-vite-3fdj)

## React
[useFetchWithAbort.tsx](https://gist.github.com/thathurtabit/0eed2c8568c409a5dd6a757c29f9564f)

## EJS
[Node.js Express EJS Layouts and Partials Tutorial](https://www.youtube.com/watch?v=lYVKbAn5Od0)


## CSS
[A Modern CSS Reset](https://andy-bell.co.uk/a-modern-css-reset/)

[CodePen Home - Accordion - height "auto" with grid](https://codepen.io/kevinpowell/pen/NWOgVga)

## BUGs
[Issue 1412729: HTML `pattern` attribute should set `v` flag for regular expressions](https://bugs.chromium.org/p/chromium/issues/detail?id=1412729)

## HTML
[Accordion Example](https://www.w3.org/WAI/ARIA/apg/patterns/accordion/examples/accordion/#support-notice-header)

## Docker
[Connecting from a Docker container to a local MongoDB](https://tsmx.net/docker-local-mongodb/#Useful_links)

[Connecting to local mongodb from docker container](https://stackoverflow.com/questions/43800164/connecting-to-local-mongodb-from-docker-container)

[Mongodb: assigning docker gateway to mongo.conf](https://www.mongodb.com/community/forums/t/mongodb-assigning-docker-gateway-to-mongo-conf/188768)

[Seccomp security profiles for Docker](https://gdevillele.github.io/engine/security/seccomp/)

[Should I use docker-compose up or run?](https://stackoverflow.com/questions/33066528/should-i-use-docker-compose-up-or-run)

[How To Remove Docker Images, Containers, and Volumes](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes)

[Auto remove container with docker-compose.yml](https://stackoverflow.com/questions/47207616/auto-remove-container-with-docker-compose-yml)

## Docker Composer
[The Complete Guide to Docker Secrets](https://earthly.dev/blog/docker-secrets/)

[How to Handle Secrets in Docker](https://blog.gitguardian.com/how-to-handle-secrets-in-docker/)

[Secret files not mounted in /run/secrets #9822](https://github.com/docker/compose/issues/9822)

[Use secrets](https://docs.docker.com/compose/use-secrets/#use-secrets)

[Docker secrets](https://spacelift.io/blog/docker-secrets)

[Set-secomp-to-unconfined-in-docker-compose](https://stackoverflow.com/questions/46053672/set-secomp-to-unconfined-in-docker-compose)

[daemon configuration](https://medium.com/@sujaypillai/docker-daemon-configuration-file-f577000da655)

[is-there-a-difference-if-we-setup-seccomp-on-docker-daemon-or-directly-when-run](https://stackoverflow.com/questions/77150775/is-there-a-difference-if-we-setup-seccomp-on-docker-daemon-or-directly-when-runn)

[Using Secrets with Docker](https://render.com/docs/docker-secrets)

### Build a docker with env
[Build a docker with env](https://stackoverflow.com/questions/47968875/how-to-build-docker-with-env-file)

### Best Practices
[Dockerfile good practices for Node and NPM](https://adambrodziak.pl/dockerfile-good-practices-for-node-and-npm)

[How To Build a Node.js Application with Docker](https://www.digitalocean.com/community/tutorials/how-to-build-a-node-js-application-with-docker)

[Best Practices for working with Dockerfiles](https://medium.com/@BeNitinAgarwal/best-practices-for-working-with-dockerfiles-fb2d22b78186)

### Memomry Leaks
[Possible EventEmitter memory leak detected after updating to the latest version of Node.js](https://stackoverflow.com/questions/77388219/possible-eventemitter-memory-leak-detected-after-updating-to-the-latest-version)


### Docker container on aws
[Env variables to Docker container using secrets manager, parameter store and s3 bucket env file](https://www.youtube.com/watch?v=OUp-iXpXNBA)

[[Backend #27] Auto build & push docker image to AWS ECR with Github Actions](https://www.youtube.com/watch?v=3M4MPmSWt9E&t=14s)

[meanstack with atlas on fargate](https://github.com/mongodb-partners/MEANStack_with_Atlas_on_Fargate)


### MONGO to AWS
[Connect AWS IAM to MongoDB Atlas - Tutorial](https://www.mongodb.com/community/forums/t/connect-aws-iam-to-mongodb-atlas-tutorial/221683)

[Set Up Unified AWS Access](https://www.mongodb.com/docs/atlas/security/set-up-unified-aws-access/#:~:text=Log%20in%20to%20your%20AWS,from%20the%20list%20of%20roles.)

[Connect mongodb from AWS lambda python using IAM](https://stackoverflow.com/questions/75591618/connect-mongodb-from-aws-lambda-python-using-iam)

[Meanstack with Atlas on fargate](https://github.com/mongodb-partners/MEANStack_with_Atlas_on_Fargate/tree/main)

[How to connect mongodb to an ec2 application](https://stackoverflow.com/questions/71635788/how-to-connect-to-mongodb-atlas-cluster-from-an-ec2-application)



### AWS setups
[AWS ECS Error: No Container Instances were found in your cluster](https://stackoverflow.com/questions/36523282/aws-ecs-error-when-running-task-no-container-instances-were-found-in-your-clust)

[How to Deploy a Docker App to AWS ECS](https://www.youtube.com/watch?v=YDNSItBN15w)

### How to learn AWS
[How To Learn AWS? Starting Points for Devops, Frontend, Backend, and DE Career Paths](https://www.youtube.com/watch?v=N8lcedBPmE8)

#### 1. Regions and Availibility Zones
#### 2. Identity & Access management (IAM)
#### 3. Cloudwatch Logs
#### 4. Cloud Development Kit (CDK) / CloudFormation
