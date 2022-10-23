## Usage

```yaml
version: '2'
plugins:
- name: py
  wasm:
    url: https://github.com/tabbed/sqlc-gen-python/releases/download/v0.16.0-alpha/sqlc-gen-python.wasm
    sha256: 4fb54ee7d25b4d909b59a8271ebee60ad76ff17b10d61632a5ca5651e4bfe438
sql:
- schema: "schema.sql"
  queries: "query.sql"
  engine: postgresql
  codegen:
  - out: src/authors
    plugin: py
    options:
      package: authors
      emit_sync_querier: true
      emit_async_querier: true
```
