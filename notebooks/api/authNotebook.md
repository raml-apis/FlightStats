---
site: https://anypoint.mulesoft.com/apiplatform/popular/admin/#/dashboard/apis/18801/versions/20074/portal/pages/33268/edit
apiNotebookVersion: 1.1.67
title: API Notebook
---

```javascript
load('https://github.com/chaijs/chai/releases/download/1.9.0/chai.js')
```

See http://chaijs.com/guide/styles/ for assertion styles

```javascript
assert = chai.assert
```

```javascript
API.createClient('client', '/apiplatform/repository/public/organizations/30/apis/18801/versions/20074/definition');
```

```javascript
APPID = prompt("Please input Access appId")
APPKEY = prompt("Please input Access appKey")
```

```javascript
function customAuthHack(o){
o.setRequestHeader("appId", APPID);
o.setRequestHeader("appKey",  APPKEY);
}
```

```javascript
API.set(client, 'beforeSend', new function(){return customAuthHack})
```

```javascript
client.airlines.rest.version("v1").json.active.get({},{headers:{"appId":"83e5dbd8",
                                                                "appKey":"c59f43472bd1c7871eb26ddbdb9c47e9"}})
```

```javascript
client.airlines.rest.version("v1").json.active.get({"appId":"83e5dbd8","appKey":"c59f43472bd1c7871eb26ddbdb9c47e9"})
```