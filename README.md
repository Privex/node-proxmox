
node-proxmox
============

NodeJs Module to interract with Proxmox VE API. Full async.

This project was previously abandoned by [@maloddon](https://github.com/maloddon). We've
picked it up at Privex Inc. for use within our own projects.

Our most recent changes included replacing the raw HTTP with the well known Node
[request](https://github.com/request/request) library, which helped us resolve issues
with certain Proxmox endpoints.

Usage
============

```
npm install --save proxmox-node
```

```
var px = require('proxmox-node')('hostname', 'username', 'authtype', 'password');

px.get('/nodes/', callback(data));
px.post('/nodes/{node}/storage/{storage}/content/{volume}', body, callback(data));
px.put('/nodes/{node}/dns', body, callback(data));
px.del('/nodes/{node}/storage/{storage}/content/{volume}', callback(data));
```

Resources
============

Proxmox API documentation : http://pve.proxmox.com/pve-docs/api-viewer/index.html
