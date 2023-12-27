

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


## Works in Playground

[link](https://workers.cloudflare.com/playground#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-MYH8hJLAHNJHYY5VIaT6GYO4IAA)

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
