# Empire

```bash
version="v3.6.0"

# with persistent storage
docker create -v /empire --name data bcsecurity/empire:${version}
docker run -it --volumes-from data bcsecurity/empire:${version} /bin/bash
```
