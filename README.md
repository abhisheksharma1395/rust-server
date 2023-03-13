## Usage

Defaults:
- HTTP server listens to `0.0.0.0:8080`.
- HTTP request headers return with the response.
- GET requests have no body content.

```console
echo-server [-p|--port=8080] [-b|--body="Custom GET response body"]
```

> All HTTP verbs are supported.

#### `GET` request

```console
curl -X GET localhost:8080
```

#### `POST` request

```console
curl -X POST -H "Content-Type: application/json" -d '{"hello": "world"}' localhost:8080
```

## Docker

You can run a precompiled image from Docker hub:

```console
docker run --rm -p 8080:8080 --name rust-server adroitx/rust-server:latest
```

Or build the image local:

```console
docker build -t rust-server .
docker run --rm -p 8080:8080 --name rust-server adroitx/rust-server:latest
```