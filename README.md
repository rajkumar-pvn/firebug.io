firebug.io
==========

**Status: DEV**

This project contains everything needed to operate http://firebug.io


Install
-------

Clone:

	git clone git@github.com:firebug/firebug.io.git firebug.io
	cd firebug.io

Install:

	bin/install.sh

Activate:

	source bin/activate.sh

Configure:

	# Add to ../firebug.io.profile.json`
	{
	    "services": {
	        "1-io.pinf": {
	            "io.pinf.server.auth": {
	                "config": {
	                    "passport": {
	                        "github": {
	                            "configUrl": "https://github.com/organizations/*/settings/applications/*",
	                            "clientID": "*",
	                            "clientSecret": "*"
	                        }
	                    }
	                }
	            }
	        }
	    }
	}	

Deploy for dev:

	pio deploy

Deploy for production (i.e. to maintain `firebug.io`):

	# Add to ../firebug.io.profile.json`
	{
	    "config": {
	        "pio": {
	            "hostname": "firebug.io"
	        }
	    }
	}


Catalogs
--------

The following catalogs are exported:

	curl -v -H "x-pio.catalog-key: 37a1043d-596a-4bd5-bf60-6d057b30dec2" \
	  http://assets.firebug.io/catalog/os-inception~dev

	curl -v -H "x-pio.catalog-key: 37a1043d-596a-4bd5-bf60-6d057b30dec2" \
	  http://assets.firebug.io/catalog/os-inception~int

	curl -v -H "x-pio.catalog-key: 37a1043d-596a-4bd5-bf60-6d057b30dec2" \
	  http://assets.firebug.io/catalog/os-inception~prod

	curl -v -H "x-pio.catalog-key: 37a1043d-596a-4bd5-bf60-6d057b30dec2" \
	  http://assets.firebug.io/catalog/os-inception~rev~*

	curl -v -H "x-pio.catalog-key: 1322705f-cac1-4028-a2c8-1aee1235119c" \
	  http://assets.firebug.io/catalog/io-devcomp~dev

	curl -v -H "x-pio.catalog-key: 1322705f-cac1-4028-a2c8-1aee1235119c" \
	  http://assets.firebug.io/catalog/io-devcomp~int

	curl -v -H "x-pio.catalog-key: 1322705f-cac1-4028-a2c8-1aee1235119c" \
	  http://assets.firebug.io/catalog/io-devcomp~prod

	curl -v -H "x-pio.catalog-key: 1322705f-cac1-4028-a2c8-1aee1235119c" \
	  http://assets.firebug.io/catalog/io-devcomp~rev~*


License
=======

Copyright (c) 2014, Mozilla Foundation

License: BSD License

Original code donated to Mozilla Foundation by [Christoph Dorn](http://christophdorn.com).

