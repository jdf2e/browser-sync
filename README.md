
## Difference with offical version

We want to use the External and External UI when we do local development. So we cut the dns detect and return the options `{online: true}` derectly. 

还因为国内访问不到Google，而bs判断是否online是采用解析www.google.com的dns的策略。

In lib/async.js, we replaced the code in getOnlineStatus method by: 

```js
done(null, {
    options: {
        online: true
    }
});
```

It's the only difference with the offical version.

## Features
Please visit [BrowserSync/browser-sync](https://github.com/BrowserSync/browser-sync) to get the latest version.
Please visit [browsersync.io](http://browsersync.io) for a full run-down of features.

## Forked version

2.18.6
