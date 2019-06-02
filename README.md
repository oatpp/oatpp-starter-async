# oatpp-starter-async [![Build Status](https://dev.azure.com/lganzzzo/lganzzzo/_apis/build/status/oatpp.oatpp-starter-async?branchName=master)](https://dev.azure.com/lganzzzo/lganzzzo/_build?definitionId=11&branchName=master)

oatpp Async-API starter project.

More about oat++:
- Website: [https://oatpp.io](https://oatpp.io)
- Docs: [https://oatpp.io/docs/start](https://oatpp.io/docs/start)
- Oat++ Repo: [https://github.com/oatpp/oatpp](https://github.com/oatpp/oatpp)

## Before you start

Read:
- [oatpp Async](https://oatpp.io/docs/async)
- [oatpp Coroutines](https://oatpp.io/docs/oatpp-coroutines)
- [ApiController](https://oatpp.io/docs/component/api-controller) - ```ENDPOINT_ASYNC``` part.

## Overview

### Project layout

```
- CMakeLists.txt                        // projects CMakeLists.txt
- src/                                  // source folder
- test/                                 // test folder
- utility/install-oatpp-modules.sh      // utility script to install required oatpp-modules.
```
```
- src/
    |
    |- controller/              // Folder containing UserController where all endpoints are declared
    |- dto/                     // DTOs are declared here
    |- AppComponent.hpp         // Service config
    |- Logger.hpp               // Application Logger
    |- App.cpp                  // main() is here
    
```

---

### Build and Run

#### Using CMake

**Requires** 

- `oatpp` module installed. You may run `utility/install-oatpp-modules.sh` 
script to install required oatpp modules.

```
$ mkdir build && cd build
$ cmake ..
$ make 
$ ./my-project-exe  # - run application.

```

#### In Docker

```
$ docker build -t oatpp-starter-async .
$ docker run -p 8000:8000 -t oatpp-starter-async
```
