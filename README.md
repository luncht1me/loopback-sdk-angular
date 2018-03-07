# LoopBack AngularJS SDK

**NOTE: The loopback-sdk-angular module supersedes [loopback-angular](https://www.npmjs.org/loopback-angular). Please update your package.json accordingly.**

The JavaScript AngularJS SDK provides an API based on
[ngResource.$resource](http://docs.angularjs.org/api/ngResource.$resource)
that enable your AngularJS app to access a
[LoopBack](http://loopback.io) server application.

The client is dynamic, in other words it automatically includes all the
LoopBack models and methods you've defined on your server.
You don't have to manually write any static code.

See the official [LoopBack AngularJS SDK
documentation](http://loopback.io/doc/en/lb2/AngularJS-JavaScript-SDK.html)
for more information.

## Mailing List

Discuss features and ask questions on [LoopBack Forum](https://groups.google.com/forum/#!forum/loopbackjs).

#### Custom AuthHeader:

Accepts an `options.authHeader` to define what lb-services.js should key the authorization token by in the headers. Used in conjunction with setting loopback token middleware to accept custom auth headers.

ie:
```js
// server.js
server.use(
	loopback.token({
		headers: ['access_token']
	})
);
```

```js
// gulp-loopback-sdk-angular (forked version to accept authHeader option) task
// [...]
.pipe(lbAngular({authHeader: 'access_token'})) 
// [...]
```