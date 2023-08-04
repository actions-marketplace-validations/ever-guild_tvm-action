# TVM Action

## Toolchain

- fift, func, lite-client, tonlib-cli, etc `v2023.06`
- solc, sold `v0.71.0`
- tvm_linker `v0.20.5`
- tonos-cli `v0.35.4`

## Example usage

### Docker

```bash
echo '4 10 * 2 + .s' | docker run --rm -i ghcr.io/ever-guild/tvm-action fift
```

### GitHub Actions

```yaml
name: CI

jobs:
  test:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v3
      - uses: ever-guild/tvm-action@v1
        with:
          args: echo '4 10 * 2 + .s' | fift
```
