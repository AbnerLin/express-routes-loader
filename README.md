# Express Routes Loader

    Load all routes in directory.

## Installation
    
    npm install @abnerlin/express-routes-loader


## Usage
    
```
const app = express();
const expressRouteLoader = require('@abnerlin/express-routes-loader')(app);
    
...

```

### Load all routes in direcotry

```
expressRouteLoader.dir(path.join(__dirname, 'routes')); // which 'routes' is directory path.
```

### Load routes with specify file

```
expressRouteLoader.file(path.join(__dirname, 'routes', 'auth')); // which 'routes/auth' is file path.

```

### Export url path
```
const express = require('express');
const router = express.Router();

router.post('/login', function(req, res) {
        ...
});

router.root = '/auth';  // this is url path which must export.

module.exports = router;
```