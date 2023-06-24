![image](https://github.com/pipo7/dockerAPIauthorization/assets/33145118/26cb9da2-3d74-4485-804e-f100f88c793d)# dockerAPIauthorization

use Cazbin Authz Plugin

# steps

start the Docker API
```cd /lib/systemd/system/docker.service 
ExecStart=/usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock -H=tcp://0.0.0.0:8080```

Generate certs for TLS docker API

Install as in https://github.com/casbin/casbin-authz-plugin

 ```systemctl daemon-reload ```
``` systemctl enable casbin-authz-plugin ```
``` systemctl start casbin-authz-plugin ```

Authentication Flow: https://docs.docker.com/engine/extend/plugins_authorization/ ![image](https://github.com/pipo7/dockerAPIauthorization/assets/33145118/2a255f84-d390-4072-bbeb-905cd0044442)



