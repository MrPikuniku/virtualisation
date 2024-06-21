# virtualisation
Usage de Docker

Commandes de l'invite: 
PS C:\Users\ms284034\Desktop\virtualisation\tp1> docker run -it --rm --name container-tp-1 node:alpine node /app/main.js
node:internal/modules/cjs/loader:1145                                                    Recherch  throw err;                                                                            rche du p  ^                                                                                     NFO-NEV-2Error: Cannot find module '/app/main.js'
    at Module._resolveFilename (node:internal/modules/cjs/loader:1142:15)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:142:1    at node:internal/main/run_main_module:28:49 {
  code: 'MODULE_NOT_FOUND',
}

Node.js v21.7.1
C:\Users\ms284034\Desktop\virtualisation\tp1
PS C:\Users\ms284034\Desktop\virtualisation\tp1> docker run -it --rm -v "$pwd\main.js:/app/main.js" --name container-tp-1 node:alpine node /app/main.js node /app/main.js
Server is running on http://0.0.0.0:8000
^CServer shutdown                                                                                                                    1 node:alpine node /app/main.js
PS C:\Users\ms284034\Desktop\virtualisation\tp1> docker run -it --rm -p 3000:8000 -v "$pwd\main.js:/app/main.js" --name container-tp-1 node:alpine node /app/main.js
Server is running on http://0.0.0.0:8000                                                                                             1 node:alpine node /app/main.js
^CServer shutdown
PS C:\Users\ms284034\Desktop\virtualisation\tp1> docker run -it --rm -p 4000:8000 -v "$pwd\main.js:/app/main.js" --name container-tp-1 node:alpine node /app/main.js
Server is running on http://0.0.0.0:8000

Microsoft Windows [version 10.0.19045.3930]
(c) Microsoft Corporation. Tous droits réservés.

C:\Users\ms284034>docker pull node:alpine
alpine: Pulling from library/node
4abcf2066143: Pull complete
1c6d0e08288a: Pull complete
25f5c574f7c4: Pull complete
37160e49a8ba: Pull complete
Digest: sha256:577f8eb599858005100d84ef3fb6bd6582c1b6b17877a393cdae4bfc9935f068
Status: Downloaded newer image for node:alpine
docker.io/library/node:alpine

C:\Users\ms284034>node -i
Welcome to Node.js v18.16.0.
Type ".help" for more information.
> JSON
Object [JSON] {}



> 'Je me trouve actuellement dans le répertoire ${process.cwd()}'
'Je me trouve actuellement dans le répertoire ${process.cwd()}'
> 'Je me trouve actuellement dans le répertoire ${process.cwd()}'
'Je me trouve actuellement dans le répertoire ${process.cwd()}'
> 'Je me trouve actuellement dans le répertoire ${process.cwd()}'
'Je me trouve actuellement dans le répertoire ${process.cwd()}'
> 'Je me trouve actuellement dans le répertoire ${process.cwd()}'
'Je me trouve actuellement dans le répertoire ${process.cwd()}'
> `Je me trouve actuellement dans le répertoire ${process.cwd()}
...
...
...
...
>
(To exit, press Ctrl+C again or Ctrl+D or type .exit)
>

C:\Users\ms284034>docker pull node:alpine     `
"docker pull" requires exactly 1 argument.
See 'docker pull --help'.

Usage:  docker pull [OPTIONS] NAME[:TAG|@DIGEST]

Download an image from a registry

C:\Users\ms284034>node -i
Welcome to Node.js v18.16.0.
Type ".help" for more information.
> `Je me truve actuellement dans le répertoire ${process.cwd()}`
'Je me truve actuellement dans le répertoire C:\\Users\\ms284034'
>
(To exit, press Ctrl+C again or Ctrl+D or type .exit)
>

C:\Users\ms284034>docker run -it --rm --name container-tp-1 node:alpine
Welcome to Node.js v21.7.1.
Type ".help" for more information.
>  `Je me truve actuellement dans le répertoire ${process.cwd()}`
'Je me truve actuellement dans le répertoire /'
> npm i -D @types/node
npm should be run outside of the Node.js REPL, in your normal shell.
(Press Ctrl+D to exit.)
> npm i -D @types/node
npm should be run outside of the Node.js REPL, in your normal shell.
(Press Ctrl+D to exit.)
> npm i -D @types/node
npm should be run outside of the Node.js REPL, in your normal shell.
(Press Ctrl+D to exit.)
>

C:\Users\ms284034>npm i -D @types/node

added 2 packages in 388ms

C:\Users\ms284034>docker run -it --rm --name container-tp-1 node:alpine
Welcome to Node.js v21.7.1.
Type ".help" for more information.
>
(To exit, press Ctrl+C again or Ctrl+D or type .exit)
>

C:\Users\ms284034>
C:\Users\ms284034>docker run -it --rm --name container-tp-1 node:alpine node /app/main.js
node:internal/modules/cjs/loader:1145
  throw err;
  ^

Error: Cannot find module '/app/main.js'
    at Module._resolveFilename (node:internal/modules/cjs/loader:1142:15)
    at Module._load (node:internal/modules/cjs/loader:983:27)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:142:12)
    at node:internal/main/run_main_module:28:49 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}

Node.js v21.7.1

C:\Users\ms284034>docker run -p 0.0.0.0:8000/tcp node:alpine




