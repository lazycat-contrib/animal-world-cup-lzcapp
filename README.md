# Animal World Cup for LazyCat

LazyCat LPK v2 packaging for [Animal World Cup](https://github.com/NeoXu954/animal-world-cup), an animal football simulator.

The application serves the game on port `13000`. Public-room HTTP and WebSocket endpoints are exposed through the same LazyCat HTTPS application domain and forwarded to the relay on port `13002`.

## Build

```bash
lzc-cli project release -o dist/application.lpk
```

## Publishing

The GitHub Actions workflow checks stable image tags from `docker.io/918178/animal-world-cup`, verifies the configured mirror for Linux amd64, creates a versioned GitHub Release asset, and publishes only to the MiaoMiao private store.

Required GitHub Secrets:

- `APPSTORE_URL`
- `APPSTORE_TOKEN`
