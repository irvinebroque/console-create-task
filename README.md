

## Works in Wrangler

```sh
➜  console-create-task git:(main) npm run dev

> console-create-task@0.0.0 dev
> wrangler dev

 ⛅️ wrangler 3.22.1
-------------------
⎔ Starting local server...
[wrangler:inf] Ready on http://localhost:8787
stuff
```

## Works in Quick Editor


## Fails in just `workerd`

```sh
npx workerd@latest serve config.capnp --verbose
workerd/io/worker.c++:1771: info: uncaught exception; source = Uncaught (in promise); exception = TypeError: console.createTask is not a function
```


## Fails in production

`https://console-create-task.roundtrip.workers.dev` (1101 error)

```json
  "exceptions": [
    {
      "name": "TypeError",
      "message": "console.createTask is not a function",
      "timestamp": 1703702255324
    }
  ],
```
