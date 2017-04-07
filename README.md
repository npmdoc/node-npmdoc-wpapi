# api documentation for  [wpapi (v1.0.3)](https://github.com/wp-api/node-wpapi)  [![npm package](https://img.shields.io/npm/v/npmdoc-wpapi.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-wpapi) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-wpapi.svg)](https://travis-ci.org/npmdoc/node-npmdoc-wpapi)
#### An isomorphic JavaScript client for interacting with the WordPress REST API

[![NPM](https://nodei.co/npm/wpapi.png?downloads=true)](https://www.npmjs.com/package/wpapi)

[![apidoc](https://npmdoc.github.io/node-npmdoc-wpapi/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-wpapi_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-wpapi/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-wpapi/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-wpapi/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "K.Adam White",
        "url": "http://www.kadamwhite.com"
    },
    "bugs": {
        "url": "https://github.com/wp-api/node-wpapi/issues"
    },
    "dependencies": {
        "es6-promise": "^3.2.1",
        "li": "^1.0.1",
        "lodash.uniq": "^4.3.0",
        "node.extend": "^1.1.5",
        "parse-link-header": "^0.4.1",
        "qs": "^6.2.0",
        "route-parser": "0.0.4",
        "superagent": "^3.3.1"
    },
    "description": "An isomorphic JavaScript client for interacting with the WordPress REST API",
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "combyne": "^2.0.0",
        "grunt": "^1.0.1",
        "grunt-cli": "^1.2.0",
        "grunt-contrib-clean": "^1.0.0",
        "grunt-contrib-jshint": "^1.0.0",
        "grunt-contrib-yuidoc": "^1.0.0",
        "grunt-zip": "^0.17.1",
        "istanbul": "^0.4.4",
        "jscs": "^3.0.6",
        "jscs-stylish": "^0.3.1",
        "jshint": "^2.9.2",
        "jshint-stylish": "^2.2.0",
        "json-loader": "^0.5.4",
        "kramed": "^0.5.6",
        "load-grunt-tasks": "^3.5.0",
        "lodash.reduce": "^4.6.0",
        "minimist": "^1.2.0",
        "mocha": "^2.5.3",
        "prompt": "^1.0.0",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0",
        "webpack": "^1.13.1"
    },
    "directories": {},
    "dist": {
        "shasum": "e2ffdfb1181e2856140e78e1c74406d3839ba226",
        "tarball": "https://registry.npmjs.org/wpapi/-/wpapi-1.0.3.tgz"
    },
    "gitHead": "e2c89fd650baf03e72ef730cb7539b9b593162de",
    "homepage": "https://github.com/wp-api/node-wpapi",
    "keywords": [
        "api",
        "client",
        "cms",
        "wordpress"
    ],
    "license": "MIT",
    "main": "wpapi.js",
    "maintainers": [
        {
            "name": "kadamwhite",
            "email": "adam@kadamwhite.com"
        }
    ],
    "name": "wpapi",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/wp-api/node-wpapi.git"
    },
    "scripts": {
        "build": "webpack && webpack --config webpack.config.minified.js",
        "docs": "grunt docs",
        "jekyll": "node bin/jekyll",
        "jscs": "jscs Gruntfile.js wpapi.js bin build lib tests --reporter node_modules/jscs-stylish/jscs-stylish.js",
        "jshint": "jshint --reporter=node_modules/jshint-stylish/index.js Gruntfile.js wpapi.js bin build lib tests",
        "lint": "npm run jshint && npm run jscs || true",
        "mocha": "_mocha tests --recursive --reporter=nyan",
        "pretest": "npm run lint",
        "release-docs": "node build/scripts/release-docs",
        "release-npm": "npm run build && npm test && npm publish",
        "test": "istanbul cover _mocha -- tests --recursive --reporter=nyan",
        "test:all": "_mocha tests --recursive --reporter=nyan",
        "test:ci": "npm run lint && istanbul cover _mocha -- tests/unit --recursive --reporter=list",
        "test:integration": "_mocha tests/integration --recursive --reporter=nyan",
        "test:unit": "_mocha tests/unit --recursive --reporter=nyan",
        "update-default-routes-json": "node ./lib/data/update-default-routes-json",
        "watch": "grunt watch",
        "zip": "npm run build && grunt zip"
    },
    "version": "1.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module wpapi](#apidoc.module.wpapi)
1.  [function <span class="apidocSignatureSpan">wpapi.</span>discover ( url )](#apidoc.element.wpapi.discover)
1.  [function <span class="apidocSignatureSpan">wpapi.</span>site ( endpoint, routes )](#apidoc.element.wpapi.site)
1.  object <span class="apidocSignatureSpan">wpapi.</span>autodiscovery
1.  object <span class="apidocSignatureSpan">wpapi.</span>endpoint_factories
1.  object <span class="apidocSignatureSpan">wpapi.</span>endpoint_request
1.  object <span class="apidocSignatureSpan">wpapi.</span>http_transport
1.  object <span class="apidocSignatureSpan">wpapi.</span>path_part_setter
1.  object <span class="apidocSignatureSpan">wpapi.</span>resource_handler_spec
1.  object <span class="apidocSignatureSpan">wpapi.</span>route_tree
1.  object <span class="apidocSignatureSpan">wpapi.</span>transport

#### [module wpapi.autodiscovery](#apidoc.module.wpapi.autodiscovery)
1.  [function <span class="apidocSignatureSpan">wpapi.autodiscovery.</span>locateAPIRootHeader ( response )](#apidoc.element.wpapi.autodiscovery.locateAPIRootHeader)

#### [module wpapi.endpoint_factories](#apidoc.module.wpapi.endpoint_factories)
1.  [function <span class="apidocSignatureSpan">wpapi.endpoint_factories.</span>generate ( routesByNamespace )](#apidoc.element.wpapi.endpoint_factories.generate)

#### [module wpapi.endpoint_request](#apidoc.module.wpapi.endpoint_request)
1.  [function <span class="apidocSignatureSpan">wpapi.endpoint_request.</span>create ( handlerSpec, resource, namespace )](#apidoc.element.wpapi.endpoint_request.create)

#### [module wpapi.http_transport](#apidoc.module.wpapi.http_transport)
1.  [function <span class="apidocSignatureSpan">wpapi.http_transport.</span>delete ( wpreq, data, callback )](#apidoc.element.wpapi.http_transport.delete)
1.  [function <span class="apidocSignatureSpan">wpapi.http_transport.</span>get ( wpreq, callback )](#apidoc.element.wpapi.http_transport.get)
1.  [function <span class="apidocSignatureSpan">wpapi.http_transport.</span>head ( wpreq, callback )](#apidoc.element.wpapi.http_transport.head)
1.  [function <span class="apidocSignatureSpan">wpapi.http_transport.</span>post ( wpreq, data, callback )](#apidoc.element.wpapi.http_transport.post)
1.  [function <span class="apidocSignatureSpan">wpapi.http_transport.</span>put ( wpreq, data, callback )](#apidoc.element.wpapi.http_transport.put)

#### [module wpapi.path_part_setter](#apidoc.module.wpapi.path_part_setter)
1.  [function <span class="apidocSignatureSpan">wpapi.path_part_setter.</span>create ( node )](#apidoc.element.wpapi.path_part_setter.create)

#### [module wpapi.resource_handler_spec](#apidoc.module.wpapi.resource_handler_spec)
1.  [function <span class="apidocSignatureSpan">wpapi.resource_handler_spec.</span>create ( routeDefinition, resource )](#apidoc.element.wpapi.resource_handler_spec.create)

#### [module wpapi.route_tree](#apidoc.module.wpapi.route_tree)
1.  [function <span class="apidocSignatureSpan">wpapi.route_tree.</span>build ( routes )](#apidoc.element.wpapi.route_tree.build)



# <a name="apidoc.module.wpapi"></a>[module wpapi](#apidoc.module.wpapi)

#### <a name="apidoc.element.wpapi.discover"></a>[function <span class="apidocSignatureSpan">wpapi.</span>discover ( url )](#apidoc.element.wpapi.discover)
- description and source-code
```javascript
discover = function ( url ) {
	// local placeholder for API root URL
	var endpoint;

	// Try HEAD request first, for smaller payload: use WPAPI.site to produce
	// a request that utilizes the defined HTTP transports
	var req = WPAPI.site( url ).root();
	return req.headers()
		.catch(function() {
			// On the hypothesis that any error here is related to the HEAD request
			// failing, provisionally try again using GET because that method is
			// more widely supported
			return req.get();
		})
		// Inspect response to find API location header
		.then( autodiscovery.locateAPIRootHeader )
		.then(function( apiRootURL ) {
			// Set the function-scope variable that will be used to instantiate
			// the bound WPAPI instance,
			endpoint = apiRootURL;

			// then GET the API root JSON object
			return WPAPI.site( apiRootURL ).root().get();
		})
		.then(function( apiRootJSON ) {
			// Instantiate & bootstrap with the discovered methods
			return new WPAPI({
				endpoint: endpoint,
				routes: apiRootJSON.routes
			});
		})
		.catch(function( err ) {
			console.error( err );
			if ( endpoint ) {
				console.warn( 'Endpoint detected, proceeding despite error...' );
				console.warn( 'Binding to ' + endpoint + ' and assuming default routes' );
				return new WPAPI.site( endpoint );
			}
			throw new Error( 'Autodiscovery failed' );
		});
}
```
- example usage
```shell
...
process.env.NODE_TLS_REJECT_UNAUTHORIZED = "0";
'''

### Auto-Discovery

It is also possible to leverage the [capability discovery](https://developer.wordpress.org/rest-api/using-the-rest-api/discovery
/) features of the API to automatically detect and add setter methods for your custom routes, or routes added by plugins.

To utilize the auto-discovery functionality, call 'WPAPI.discover()' with a URL within a WordPress REST API-enabled site:

'''js
var apiPromise = WPAPI.discover( 'http://my-site.com' );
'''
If auto-discovery succeeds this method returns a promise that will be resolved with a WPAPI client instance object configured specifically
 for your site. You can use that promise as the queue that your client instance is ready, then use the client normally within the
 '.then' callback.

**Custom Routes** will be detected by this process, and registered on the client. To prevent name conflicts, only routes in the '
wp/v2' namespace will be bound to your instance object itself. The rest can be accessed through the '.namespace' method on the WPAPI
 instance, as demonstrated below.
...
```

#### <a name="apidoc.element.wpapi.site"></a>[function <span class="apidocSignatureSpan">wpapi.</span>site ( endpoint, routes )](#apidoc.element.wpapi.site)
- description and source-code
```javascript
site = function ( endpoint, routes ) {
	return new WPAPI({
		endpoint: endpoint,
		routes: routes
	});
}
```
- example usage
```shell
...
/**
* Convenience method for making a new WPAPI instance
*
* @example
* These are equivalent:
*
*     var wp = new WPAPI({ endpoint: 'http://my.blog.url/wp-json' });
*     var wp = WPAPI.site( 'http://my.blog.url/wp-json' );
*
* 'WPAPI.site' can take an optional API root response JSON object to use when
* bootstrapping the client's endpoint handler methods: if no second parameter
* is provided, the client instance is assumed to be using the default API
* with no additional plugins and is initialized with handlers for only those
* default API routes.
*
...
```



# <a name="apidoc.module.wpapi.autodiscovery"></a>[module wpapi.autodiscovery](#apidoc.module.wpapi.autodiscovery)

#### <a name="apidoc.element.wpapi.autodiscovery.locateAPIRootHeader"></a>[function <span class="apidocSignatureSpan">wpapi.autodiscovery.</span>locateAPIRootHeader ( response )](#apidoc.element.wpapi.autodiscovery.locateAPIRootHeader)
- description and source-code
```javascript
function locateAPIRootHeader( response ) {
	// Define the expected link rel value per http://v2.wp-api.org/guide/discovery/
	var rel = 'https://api.w.org/';

	// Extract & parse the response link headers
	var link = response.link || ( response.headers && response.headers.link );
	var headers = parseLinkHeader( link );
	var apiHeader = headers && headers[ rel ];

	if ( apiHeader && apiHeader.url ) {
		return apiHeader.url;
	}

	throw new Error( 'No header link found with rel="https://api.w.org/"' );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wpapi.endpoint_factories"></a>[module wpapi.endpoint_factories](#apidoc.module.wpapi.endpoint_factories)

#### <a name="apidoc.element.wpapi.endpoint_factories.generate"></a>[function <span class="apidocSignatureSpan">wpapi.endpoint_factories.</span>generate ( routesByNamespace )](#apidoc.element.wpapi.endpoint_factories.generate)
- description and source-code
```javascript
function generateEndpointFactories( routesByNamespace ) {

	return objectReduce( routesByNamespace, function( namespaces, routeDefinitions, namespace ) {

		// Create
		namespaces[ namespace ] = objectReduce( routeDefinitions, function( handlers, routeDef, resource ) {

			var handlerSpec = createResourceHandlerSpec( routeDef, resource );

			var EndpointRequest = createEndpointRequest( handlerSpec, resource, namespace );

			// "handler" object is now fully prepared; create the factory method that
			// will instantiate and return a handler instance
			handlers[ resource ] = function( options ) {
				return new EndpointRequest( extend( {}, this._options, options ) );
			};

			// Expose the constructor as a property on the factory function, so that
			// auto-generated endpoint request constructors may be further customized
			// when needed
			handlers[ resource ].Ctor = EndpointRequest;

			return handlers;
		}, {} );

		return namespaces;
	}, {} );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wpapi.endpoint_request"></a>[module wpapi.endpoint_request](#apidoc.module.wpapi.endpoint_request)

#### <a name="apidoc.element.wpapi.endpoint_request.create"></a>[function <span class="apidocSignatureSpan">wpapi.endpoint_request.</span>create ( handlerSpec, resource, namespace )](#apidoc.element.wpapi.endpoint_request.create)
- description and source-code
```javascript
function createEndpointRequest( handlerSpec, resource, namespace ) {

	// Create the constructor function for this endpoint
	function EndpointRequest( options ) {
		WPRequest.call( this, options );

		<span class="apidocCodeCommentSpan">/**
		 * Semi-private instance property specifying the available URL path options
		 * for this endpoint request handler, keyed by ascending whole numbers.
		 *
		 * @property _levels
		 * @type {object}
		 * @private
		 */
</span>		this._levels = handlerSpec._levels;

		// Configure handler for this endpoint's root URL path & set namespace
		this
			.setPathPart( 0, resource )
			.namespace( namespace );
	}

	inherit( EndpointRequest, WPRequest );

	// Mix in all available shortcut methods for GET request query parameters that
	// are valid within this endpoint tree
	if ( typeof handlerSpec._getArgs === 'object' ) {
		Object.keys( handlerSpec._getArgs ).forEach(function( supportedQueryParam ) {
			var mixinsForParam = mixins[ supportedQueryParam ];

			// Only proceed if there is a mixin available AND the specified mixins will
			// not overwrite any previously-set prototype method
			if ( typeof mixinsForParam === 'object' ) {
				Object.keys( mixinsForParam ).forEach(function( methodName ) {
					applyMixin( EndpointRequest.prototype, methodName, mixinsForParam[ methodName ] );
				});
			}
		});
	}

	Object.keys( handlerSpec._setters ).forEach(function( setterFnName ) {
		// Only assign setter functions if they do not overwrite preexisting methods
		if ( ! EndpointRequest.prototype[ setterFnName ] ) {
			EndpointRequest.prototype[ setterFnName ] = handlerSpec._setters[ setterFnName ];
		}
	});

	return EndpointRequest;
}
```
- example usage
```shell
...
    // do something with the returned posts
}).catch(function( err ) {
    // handle error
});
'''
The 'wp' object has endpoint handler methods for every endpoint that ships with the default WordPress REST API plugin.

Once you have used the chaining methods to describe a resource, you may call '.create()', '.get()', '.update()' or '.delete()'
to send the API request to create, read, update or delete content within WordPress. These methods are documented in further detail
 below.

### Self-signed (Insecure) HTTPS Certificates

In a case where you would want to connect to a HTTPS WordPress installation that has a self-signed certificate (insecure), you will
 need to force a connection by placing the following line before you make any 'wp' calls.

'''javascript
process.env.NODE_TLS_REJECT_UNAUTHORIZED = "0";
...
```



# <a name="apidoc.module.wpapi.http_transport"></a>[module wpapi.http_transport](#apidoc.module.wpapi.http_transport)

#### <a name="apidoc.element.wpapi.http_transport.delete"></a>[function <span class="apidocSignatureSpan">wpapi.http_transport.</span>delete ( wpreq, data, callback )](#apidoc.element.wpapi.http_transport.delete)
- description and source-code
```javascript
function _httpDelete( wpreq, data, callback ) {
	if ( ! callback && typeof data === 'function' ) {
		callback = data;
		data = null;
	}
	checkMethodSupport( 'delete', wpreq );
	var url = wpreq.toString();
	var request = _auth( agent.del( url ), wpreq._options, true ).send( data );

	return invokeAndPromisify( request, callback, returnBody.bind( null, wpreq ) );
}
```
- example usage
```shell
...
    // do something with the returned posts
}).catch(function( err ) {
    // handle error
});
'''
The 'wp' object has endpoint handler methods for every endpoint that ships with the default WordPress REST API plugin.

Once you have used the chaining methods to describe a resource, you may call '.create()', '.get()', '.update()' or '.delete()'
to send the API request to create, read, update or delete content within WordPress. These methods are documented in further detail
 below.

### Self-signed (Insecure) HTTPS Certificates

In a case where you would want to connect to a HTTPS WordPress installation that has a self-signed certificate (insecure), you will
 need to force a connection by placing the following line before you make any 'wp' calls.

'''javascript
process.env.NODE_TLS_REJECT_UNAUTHORIZED = "0";
...
```

#### <a name="apidoc.element.wpapi.http_transport.get"></a>[function <span class="apidocSignatureSpan">wpapi.http_transport.</span>get ( wpreq, callback )](#apidoc.element.wpapi.http_transport.get)
- description and source-code
```javascript
function _httpGet( wpreq, callback ) {
	checkMethodSupport( 'get', wpreq );
	var url = wpreq.toString();

	var request = _auth( agent.get( url ), wpreq._options );

	return invokeAndPromisify( request, callback, returnBody.bind( null, wpreq ) );
}
```
- example usage
```shell
...
'''
Once an instance is constructed, you can chain off of it to construct a specific request. (Think of it as a query-builder for WordPress
!)

We support requesting posts using either a callback-style or promise-style syntax:

'''javascript
// Callbacks
wp.posts().get(function( err, data ) {
    if ( err ) {
        // handle err
    }
    // do something with the returned posts
});

// Promises
...
```

#### <a name="apidoc.element.wpapi.http_transport.head"></a>[function <span class="apidocSignatureSpan">wpapi.http_transport.</span>head ( wpreq, callback )](#apidoc.element.wpapi.http_transport.head)
- description and source-code
```javascript
function _httpHead( wpreq, callback ) {
	checkMethodSupport( 'head', wpreq );
	var url = wpreq.toString();
	var request = _auth( agent.head( url ), wpreq._options );

	return invokeAndPromisify( request, callback, returnHeaders );
}
```
- example usage
```shell
...
 * @param {WPRequest} wpreq A WPRequest query object
 * @param {Function} [callback] A callback to invoke with the results of the HEAD request
 * @return {Promise} A promise to the header results of the HTTP request
 */
function _httpHead( wpreq, callback ) {
	checkMethodSupport( 'head', wpreq );
	var url = wpreq.toString();
	var request = _auth( agent.head( url ), wpreq._options );

	return invokeAndPromisify( request, callback, returnHeaders );
}

module.exports = {
	delete: _httpDelete,
	get: _httpGet,
...
```

#### <a name="apidoc.element.wpapi.http_transport.post"></a>[function <span class="apidocSignatureSpan">wpapi.http_transport.</span>post ( wpreq, data, callback )](#apidoc.element.wpapi.http_transport.post)
- description and source-code
```javascript
function _httpPost( wpreq, data, callback ) {
	checkMethodSupport( 'post', wpreq );
	var url = wpreq.toString();
	data = data || {};
	var request = _auth( agent.post( url ), wpreq._options, true );

	if ( wpreq._attachment ) {
		// Data must be form-encoded alongside image attachment
		request = objectReduce( data, function( req, value, key ) {
			return req.field( key, value );
		}, request.attach( 'file', wpreq._attachment, wpreq._attachmentName ) );
	} else {
		request = request.send( data );
	}

	return invokeAndPromisify( request, callback, returnBody.bind( null, wpreq ) );
}
```
- example usage
```shell
...
'''js
site.handler = site.registerRoute( 'myplugin/v1', 'collection/(?P<id>)', {
    // Listing any of these parameters will assign the built-in
    // chaining method that handles the parameter:
    params: [ 'before', 'after', 'author', 'parent', 'post' ]
});
// yields
site.handler().post( 8 ).author( 92 ).before( dateObj )...
'''

If you wish to set custom parameters, for example to query by the custom taxonomy 'genre', you can use the '.param()' method as
usual:

'''js
site.handler().param( 'genre', genreTermId );
'''
...
```

#### <a name="apidoc.element.wpapi.http_transport.put"></a>[function <span class="apidocSignatureSpan">wpapi.http_transport.</span>put ( wpreq, data, callback )](#apidoc.element.wpapi.http_transport.put)
- description and source-code
```javascript
function _httpPut( wpreq, data, callback ) {
	checkMethodSupport( 'put', wpreq );
	var url = wpreq.toString();
	data = data || {};

	var request = _auth( agent.put( url ), wpreq._options, true ).send( data );

	return invokeAndPromisify( request, callback, returnBody.bind( null, wpreq ) );
}
```
- example usage
```shell
...
* @return {Promise} A promise to the results of the HTTP request
*/
function _httpPut( wpreq, data, callback ) {
	checkMethodSupport( 'put', wpreq );
	var url = wpreq.toString();
	data = data || {};

	var request = _auth( agent.put( url ), wpreq._options, true ).send( data );

	return invokeAndPromisify( request, callback, returnBody.bind( null, wpreq ) );
}

/**
* @method _httpDelete
* @async
...
```



# <a name="apidoc.module.wpapi.path_part_setter"></a>[module wpapi.path_part_setter](#apidoc.module.wpapi.path_part_setter)

#### <a name="apidoc.element.wpapi.path_part_setter.create"></a>[function <span class="apidocSignatureSpan">wpapi.path_part_setter.</span>create ( node )](#apidoc.element.wpapi.path_part_setter.create)
- description and source-code
```javascript
function createPathPartSetter( node ) {
	// Local references to 'node' properties used by returned functions
	var nodeLevel = node.level;
	var nodeName = node.names[ 0 ];
	var supportedMethods = node.methods || [];
	var dynamicChildren = node.children ? Object.keys( node.children )
		.map(function( key ) {
			return node.children[ key ];
		})
		.filter(function( childNode ) {
			return childNode.namedGroup === true;
		}) : [];
	var dynamicChild = dynamicChildren.length === 1 && dynamicChildren[ 0 ];
	var dynamicChildLevel = dynamicChild && dynamicChild.level;

	if ( node.namedGroup ) {
		<span class="apidocCodeCommentSpan">/**
		 * Set a dymanic (named-group) path part of a query URL.
		 *
		 * @example
		 *
		 *     // id() is a dynamic path part setter:
		 *     wp.posts().id( 7 ); // Get posts/7
		 *
		 * @chainable
		 * @param  {String|Number} val The path part value to set
		 * @return {Object} The handler instance (for chaining)
		 */
</span>		return function( val ) {
			/* jshint validthis:true */
			this.setPathPart( nodeLevel, val );
			if ( supportedMethods.length ) {
				this._supportedMethods = supportedMethods;
			}
			return this;
		};
	} else {
		/**
		 * Set a non-dymanic (non-named-group) path part of a query URL, and
		 * set the value of a subresource if an input value is provided and
		 * exactly one named-group child node exists.
		 *
		 * @example
		 *
		 *     // revisions() is a non-dynamic path part setter:
		 *     wp.posts().id( 4 ).revisions();       // Get posts/4/revisions
		 *     wp.posts().id( 4 ).revisions( 1372 ); // Get posts/4/revisions/1372
		 *
		 * @chainable
		 * @param  {String|Number} [val] The path part value to set (if provided)
		 *                               for a subresource within this resource
		 * @return {Object} The handler instance (for chaining)
		 */
		return function( val ) {
			/* jshint validthis:true */
			// If the path part is not a namedGroup, it should have exactly one
			// entry in the names array: use that as the value for this setter,
			// as it will usually correspond to a collection endpoint.
			this.setPathPart( nodeLevel, nodeName );

			// If this node has exactly one dynamic child, this method may act as
			// a setter for that child node. 'dynamicChildLevel' will be falsy if the
			// node does not have a child or has multiple children.
			if ( val !== undefined && dynamicChildLevel ) {
				this.setPathPart( dynamicChildLevel, val );
			}
			return this;
		};
	}
}
```
- example usage
```shell
...
    // do something with the returned posts
}).catch(function( err ) {
    // handle error
});
'''
The 'wp' object has endpoint handler methods for every endpoint that ships with the default WordPress REST API plugin.

Once you have used the chaining methods to describe a resource, you may call '.create()', '.get()', '.update()' or '.delete()'
to send the API request to create, read, update or delete content within WordPress. These methods are documented in further detail
 below.

### Self-signed (Insecure) HTTPS Certificates

In a case where you would want to connect to a HTTPS WordPress installation that has a self-signed certificate (insecure), you will
 need to force a connection by placing the following line before you make any 'wp' calls.

'''javascript
process.env.NODE_TLS_REJECT_UNAUTHORIZED = "0";
...
```



# <a name="apidoc.module.wpapi.resource_handler_spec"></a>[module wpapi.resource_handler_spec](#apidoc.module.wpapi.resource_handler_spec)

#### <a name="apidoc.element.wpapi.resource_handler_spec.create"></a>[function <span class="apidocSignatureSpan">wpapi.resource_handler_spec.</span>create ( routeDefinition, resource )](#apidoc.element.wpapi.resource_handler_spec.create)
- description and source-code
```javascript
function createNodeHandlerSpec( routeDefinition, resource ) {

	var handler = {
		// A "path" is an ordered (by key) set of values composed into the final URL
		_path: {
			'0': resource
		},

		// A "level" is a level-keyed object representing the valid options for
		// one level of the resource URL
		_levels: {},

		// Objects that hold methods and properties which will be copied to
		// instances of this endpoint's handler
		_setters: {},

		// Arguments (query parameters) that may be set in GET requests to endpoints
		// nested within this resource route tree, used to determine the mixins to
		// add to the request handler
		_getArgs: routeDefinition._getArgs
	};

	// Walk the tree
	Object.keys( routeDefinition ).forEach(function( routeDefProp ) {
		if ( routeDefProp !== '_getArgs' ) {
			extractSetterFromNode( handler, routeDefinition[ routeDefProp ] );
		}
	});

	return handler;
}
```
- example usage
```shell
...
    // do something with the returned posts
}).catch(function( err ) {
    // handle error
});
'''
The 'wp' object has endpoint handler methods for every endpoint that ships with the default WordPress REST API plugin.

Once you have used the chaining methods to describe a resource, you may call '.create()', '.get()', '.update()' or '.delete()'
to send the API request to create, read, update or delete content within WordPress. These methods are documented in further detail
 below.

### Self-signed (Insecure) HTTPS Certificates

In a case where you would want to connect to a HTTPS WordPress installation that has a self-signed certificate (insecure), you will
 need to force a connection by placing the following line before you make any 'wp' calls.

'''javascript
process.env.NODE_TLS_REJECT_UNAUTHORIZED = "0";
...
```



# <a name="apidoc.module.wpapi.route_tree"></a>[module wpapi.route_tree](#apidoc.module.wpapi.route_tree)

#### <a name="apidoc.element.wpapi.route_tree.build"></a>[function <span class="apidocSignatureSpan">wpapi.route_tree.</span>build ( routes )](#apidoc.element.wpapi.route_tree.build)
- description and source-code
```javascript
function buildRouteTree( routes ) {
	return objectReduce( routes, reduceRouteTree, {} );
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
