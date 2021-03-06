# GitHub Action for Zeit

The GitHub Deployer for [Zeit](https://zeit.co/) task wraps the [Now CLI](https://github.com/zeit/now-cli) to enable common Now commands.

## Usage

```
workflow "Deploy on Now" {
  on = "push"
  resolves = ["deploy"]
}

action "deploy" {
  uses = "actions/zeit-now@master"
  secrets = [
    "ZEIT_TOKEN",
  ]
}
```

### Secrets

* `ZEIT_TOKEN` - **Required**. The token to use for authentication with the Zeit Now API ([more info](https://zeit.co/blog/introducing-api-tokens-management))

## License

The Dockerfile and associated scripts and documentation in this project are released under the [MIT License](LICENSE).

Container images built with this project include third party materials. See [THIRD_PARTY_NOTICE.md](THIRD_PARTY_NOTICE.md) for details.
