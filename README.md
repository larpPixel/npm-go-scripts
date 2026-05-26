# npm-go-scripts

Small paru-style update helpers for globally installed npm packages and Go CLIs.

## Scripts

- `npm-paru`: checks global npm packages with `npm outdated -g`, previews version and unpacked-size changes, then updates selected packages with `npm install -g`.
- `go-paru`: discovers Go binaries in `GOBIN` or `GOPATH/bin`, checks their module versions, previews binary-size changes, then updates them with `go install <package>@latest`.

## Usage

```sh
./npm-paru
./go-paru
```

Common options:

```sh
./npm-paru --check
./npm-paru --dry-run
./npm-paru --yes

./go-paru --check
./go-paru --dry-run
./go-paru --yes
```

Optional local aliases:

```sh
ln -sf "$PWD/npm-paru" ~/.local/bin/nparu
ln -sf "$PWD/go-paru" ~/.local/bin/gparu
```
