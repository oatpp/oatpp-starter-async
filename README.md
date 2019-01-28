# oatpp-starter-async [![Build Status](https://dev.azure.com/lganzzzo/lganzzzo/_apis/build/status/oatpp.oatpp-starter-async?branchName=master)](https://dev.azure.com/lganzzzo/lganzzzo/_build/latest?definitionId=11?branchName=master)
oatpp Async-API Starter template project.
config=(oatpp-coroutines plus non-blocking-IO)

## Before you start

Read:
- [oatpp Async](https://oatpp.io/docs/async)
- [oatpp Coroutines](https://oatpp.io/docs/oatpp-coroutines)
- [ApiController](https://oatpp.io/docs/component/api-controller) - ```ENDPOINT_ASYNC``` part.

## Build and run

1) Git-Clone examples repo:
```
git clone https://github.com/oatpp/oatpp-examples
```

2) Get oatpp-lib (it is included as git submodule)
```
git submodule init
git submodule update --remote --merge
```

3) CD to crud example-project
```
cd crud/
```
4) Build project
```
./build_app.sh
```
or (same as in build_app.sh)
```
g++ -std=gnu++11 \
-pthread \
`find "./lib/oatpp/" -type f -name *.cpp` \
`find "./src/" -type f -name *.cpp` \
-I "./lib" \
-I "./src" \
-D OATPP_USE_TARGET \
-D OATPP_TARGET_APP \
-D OATPP_DISABLE_ENV_OBJECT_COUNTERS \
-O2 \
-Wall \
-o run_app

chmod +x run_app
```
5) Run app
```
./run_app
```

enjoy!

## More
If you can't build app.- probably you need to [install build-essential](https://www.google.com.ua/search?q=install+build-essentials)

## Xcode, MAC
Xcode project included
