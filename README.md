# bn-tracing
 Tracing with Opentelemetry and Google Trace Exporter

# Usage
Install the npm-package and import it before express is required.

`require(bn-tracing)(options)` 

# Options
```
{
  serviceName: String (Default: default)
  debug: Bool (default: false)
  instrumentations: Array (Default: [])
}
```

# Usage example
```js
require('bn-tracing')({
  serviceName: process.env.K_SERVICE,
  instrumentations: [
    new IORedisInstrumentation(),
  ]
});
```
