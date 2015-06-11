load balancing algorithms for mesh


`npm install mesh-balance`

#### balance.rotate(workers)

Runs workers. Round-robin style.

```javascript
var workers = Array.apply(void 0, new Array(10)).map(function() {
  return mesh.wrap(function(operation, next) {
    next();
  });
});

var bus = mesh.rotate(workers);
```

#### balance.least(workers)

Runs the worker with the least number of running operations

#### balance.random(workers)

runs a random worker
