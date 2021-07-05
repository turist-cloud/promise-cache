# promise-cache

Easily convert time to milliseconds

## Examples

```javascript
import promiseCache from "@turist/promise-cache"

const LRU = require('lru-cache')
const ms = require('ms')

const cache = new LRU({
	max: 100,
	maxAge: ms('5s')
})

const getData = promiseCache(cache, async (args1, args2) => {
	// ... do async stuff

	return something;
})
```
