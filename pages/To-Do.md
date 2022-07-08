- Fix SSR
	- These modules break SSR, so they would need to be replaced.
	  ```js
	  const require = createRequire(import.meta.url)
	  const { transformWithEsbuild } = require('vite')
	  ```
		- The fix would be to import ESBuild WASM (according to Matt)