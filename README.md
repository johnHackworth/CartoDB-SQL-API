SQL API for cartodb.com
========================

Provides a nodejs based API for running SQL queries against CartoDB.

* Users are authenticated over OAuth or via an API KEY.
* Authenticated requests to this API should always be made over SSL.


core requirements
-------------
* postgres 9.0+
* cartodb 0.9.5+ (for ``CDB_QueryTables``)
* redis
* node 0.8+
* npm

Install dependencies
---------------------

```bash
npm install
```

usage
-----

Create and edit config/environments/<environment>.js from .js.example files.
You may find the ./configure script useful to make an edited copy for you,
see ```./configure --help``` for a list of supported switches.

Make sure redis is running and knows about active cartodb user.

Make sure your PostgreSQL server is running, is accessible on
the host and port specified in the <environment> file, has
a 'publicuser' role and trusts user authentication from localhost
connections.

``` bash
node [cluster.js|app.js] <environment>
```

Supported <environment> values are developement, test, production

See doc/API.md for API documentation.
For examples of use, see under test/.


tests
------

Run ```make check``` or see test/README.md

