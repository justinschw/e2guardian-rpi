#e2guardian
-------------------
<img src="http://e2guardian.org/cms/images/banners/logo-guardian.png" alt="e2g" width="100"> [e2guardian](http://e2guardian.org/) is an Open Source web content filter.

### Quickstart 
```bash
docker run --name e2guardian-rpi -d --restart=always \
  --publish 8080:8080 \
  --volume /path/to/lists:/etc/e2guardian/lists \
  --link some-squid:proxy \
  e2guardian-rpi
```
SELinux:
```bash
chcon -Rt svirt_sandbox_file_t /path/to/lists
```

