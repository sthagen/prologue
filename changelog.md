## 0.4.2

fix custom setting error (#100)

plugin.nim is for document only (#99)

fix static file serving is slow in windows(`usestd` also works)

## 0.3.8

Move `basicAuthMiddleware` from `auth/auth.nim` to `middlewares/auth.nim`. Users need to change the import clause to `import prologue/middlewares/auth`.

Setting doesn't set the default path of staticDirs anymore.

Change `Response.headers` to `ResponseHeaders`, users can initialize it with `initResponseHeaders`.


## 0.3.6

Fixes that sessionMiddleware doesn't work when user does not register session.
Fixes HttpHeaders and adds nil check.
Fixes cookies containing commas fail for asynchttpserver using base64 encode.

## 0.3.4

Fixes "Always asked to install `cookiejar` when running" #36

## 0.3.2

Fixes `resp "Hello"` will clear all attributes.

Reduces unnecessary operations.

Adds tests for cookie.

Reduces unnecessary imports and compilation time.

## 0.3.0

Windows support multi-thread HTTP server(httpx).

The route of the request is stripped. (/hello/ -> /hello)

## 0.2.8

Adds `Settings.address`, user can specify listening `address`.

OpenAPI docs allows specifying source path.

Fix `configure.getOrdefault`'s bug.

Adds more documents.

Adds more API docs.

Changes import path, allows `import prologue/middlewares` instead of 
`import prologue/middlewares/middlewares`. 

Renames `validate` to `validater`. Supports `import prologue/auth`, `import prologue/auth`, `import prologue/middlewares`, `import prologue/openapi`, `import prologue/security`, `import prologue/signing` and `import prologue/validater`.

Moves signing from the core directory.
