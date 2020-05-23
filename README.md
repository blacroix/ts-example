# Simple test with tsc

## Setup

Go to project root.

### Compile with tsc

Inside Docker container because it requires npm and typescript (tsc binary) :

```
sudo docker run --rm -i -t -v $PWD:/app -w /app node:8.12.0-alpine /bin/sh
/app # npm install -g typescript
/usr/local/bin/tsc -> /usr/local/lib/node_modules/typescript/bin/tsc
/usr/local/bin/tsserver -> /usr/local/lib/node_modules/typescript/bin/tsserver
+ typescript@3.9.3
added 1 package from 1 contributor in 69.87s
/app # tsc -b --verbose
[14:53:18] Projects in this build: 
    * tsconfig.json

[14:53:18] Project 'tsconfig.json' is out of date because output file 'build/main.js' does not exist

[14:53:18] Building project '/app/tsconfig.json'...
/app #
```

### Run local server

python -m http.server 8080

