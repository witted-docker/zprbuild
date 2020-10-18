# zprbuild

Build enviroments for zpr framework.
- `x86_64-minimal`: includes every lib needed to build a project based on core/zeromq on 64bit pc. Just cpp and python support.
- `x86_64`: support for cpp, python, golang and nim

- `crossarm-minimal`: includes every lib needed to crossbuild a project based on core/zeromq. Just cpp and python support.
- `crossarm`: support for cpp, python, golang and nim
- `crossarm64-nvidia`: includes every lib needed to crossbuild a project based on core/zeromq. Just cpp and python support. Works with NVIDIA Jetson TX2.
  
Extend as needed, for example:
```Dockerfile
FROM witted/zprbuild:crossarm

# Install cpp websocket library
RUN apt-get update && && apt-get install -y --no-install-recommends \
    libwebsocketpp-dev:armhf

```
  
  
  
© Copyright 2020 Witted Srl - All Rights Reserved

