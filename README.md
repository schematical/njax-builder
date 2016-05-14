# njax-builder
Parses various formats and creates data structures on the fly


##Example:
```
var NJaxBuilder = require('njax-builder');
var NJaxBuilderParserSwagger = require('njax-builder-parser-swagger');
var NJaxBuilderNodeSdk = require('njax-builder-nodesdk');

var builder = new NJaxBuilder();
/*
This says what kind of data were parsing
*/


builder.parser(
    new NJaxBuilderParserSwagger({

    })
)

/*
This says what were building
*/
builder.exports(
    new NJaxBuilderNodeSdk({

    })
);
/*
This builds the resulting code
*/
var options = {}
builder.run(inputSwagger, options, function(err, NodeSdk){
    if(err) throw err;

});
```
