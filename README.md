# deno-fresh-cloudflare-workers-example

Here is an example of deploying a `Deno` + `Fresh` application to `Cloudflare Workers` .

## Tech Stack

- [Deno](https://deno.com/)
- [Fresh](https://fresh.deno.dev/)
- [daisy UI](https://daisyui.com/)
- [Wrangler](https://developers.cloudflare.com/workers/wrangler/)
- [Cloudflare Workers](https://developers.cloudflare.com/workers/)
- [mise](https://mise.jdx.dev/)

## Setup

### install

```shell
# setup deno
brew install mise
mise install

git clone git@github.com:treetips/deno-fresh-cloudflare-workers-example.git
cd deno-fresh-cloudflare-workers-example && deno install
```

### .env

```shell
cat << EOT > .env
# System environment variables https://developers.cloudflare.com/workers/wrangler/system-environment-variables/
CLOUDFLARE_ACCOUNT_ID=<your account id>
CLOUDFLARE_API_TOKEN=<your api token>
EOT
```

## Usage

### Start

```shell
deno task dev
```

### Deploy

`Wrangler` is used for all deployments.

#### Automatically deploy to Cloudflare Workers with GitHub Actions

See the `.github/workflows/deploy.yaml` .

#### Deploy Cloudflare Workers from the local environment

```shell
deno task deploy
```
