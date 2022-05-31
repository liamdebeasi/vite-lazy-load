# Vite Stencil Issue

## Steps to reproduce

1. Clone repo.
2. Run `npm install`.
3. Run `npm run dev`.
4. Open `http://localhost:3000` in a browser. Observe that the following warning is logged:

```
17569|      return module[exportName];
17570|    }
17571|    return import(
   |                  ^
17572|      /* webpackInclude: /\.entry\.js$/ */
17573|      /* webpackExclude: /\.system\.entry\.js$/ */
The above dynamic import cannot be analyzed by vite.
See https://github.com/rollup/plugins/tree/master/packages/dynamic-import-vars#limitations for supported dynamic import formats. If this is intended to be left as-is, you can use the /* @vite-ignore */ comment inside the import() call to suppress this warning.
```

Note: If you do not see this warning, try restarting the server and opening the page in a new incognito tab.