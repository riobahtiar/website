---
id: node-api
title: "Node API"
---
Verdaccio подржава опцију invoqued programmatically. Nod API је уведен после верзије `verdaccio@3.0.0-alpha.10`.

## Коришћење

#### Programmatically

```js
 import startServer from 'verdaccio';   

 startServer(configJsonFormat, 6000, store, '1.0.0', 'verdaccio',
    (webServer, addrs, pkgName, pkgVersion) => {
        webServer.listen(addr.port || addr.path, addr.host, () => {
            console.log('verdaccio running');
        });
  });
```

## Остале имплементације

* [verdaccio-server](https://github.com/boringame/verdaccio-server) local npm registry proxy server

```js
// js
import * as verdaccioServer from "verdaccio-server";
verdaccioServer.start();
verdaccioServer.stop();
verdaccioServer.list();
verdaccioServer.stopAll();
verdaccioServer.show();
verdaccioServer.cli();
// windows .net2
verdaccioServer.serviceInstall();
verdaccioServer.serviceUninstall();
verdaccioServer.serviceStart();
verdaccioServer.serviceStop();
verdaccioServer.serviceRestart();
```