# nova-registry

The official package registry for Nova.

## Installing a package

```sh
nv+ install <package-name>
```

## Publishing a package

1. Make sure your package has a `novapkg.json` at the root:

```json
{
  "name": "my-package",
  "version": "1.0.0",
  "description": "Does something cool",
  "main": "src/main.nova"
}
```

2. Push your package to GitHub

3. Fork this repo and add your entry to `registry.json`:

```json
"my-package": {
  "repo": "YOUR_USERNAME/my-package",
  "description": "Does something cool",
  "latest": "1.0.0"
}
```

4. Open a Pull Request — once merged it is live instantly.

## Structure

```json
{
  "packages": {
    "package-name": {
      "repo": "github-user/repo-name",
      "description": "Short description",
      "latest": "1.0.0"
    }
  }
}
```
