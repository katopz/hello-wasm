# hello-wasm
Say hi to WASM w/ Rust

> https://blog.avareum.finance/%EF%B8%8F-hello-wasm-w-rust-4f4b275be8bf

## Build
```
rustwasmc build
```

## Deploy
```
curl --location --request POST 'https://rpc.ssvm.secondstate.io:8081/api/executables' \
--header 'Content-Type: application/octet-stream' \
--header 'SSVM-Description: say hello' \
--data-binary '@pkg/hello_wasm_bg.wasm'
```

## Run
```
curl --location --request POST 'https://rpc.ssvm.secondstate.io:8081/api/run/423/say' \
--header 'Content-Type: text/plain' \
--data-raw 'Second State FaaS'
```