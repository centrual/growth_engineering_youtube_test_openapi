# Growth Engineering Youtube Test - OpenAPI Declarations

Hello Growth Engineering 🖐

This repository stores [OpenAPI](https://swagger.io/specification/) declarations.

It automatically generates a rest client uses axios using [openapi-generator](https://openapi-generator.tech/) via Github Actions. OpenAPI generator uses the [typescript-axios generator](https://openapi-generator.tech/docs/generators/typescript-axios).

---

## Project Structure

Because the API key sharing is insecure I split the project into 3 parts. This parts are:

1. [Frontend](https://github.com/centrual/growth_engineering_youtube_test_frontend)
2. OpenAPI Declarations *
3. [Backend](https://github.com/centrual/growth_engineering_youtube_test_server)

---

## Generating Laravel Server

To generate server package with `php-laravel` template you can use the following command in CLI:

```
npx openapi-generator-cli generate -i Growth-Engineering-Youtube-Test-V2.yaml -g php-laravel -c php_laravel_server.config.json -o php_laravel_server
```

---

## Package Installation

Firstly please create a new token [from this page](https://github.com/settings/tokens/new). Only `read:packages` scope is enough to install the rest client package.

Then please create a ".npmrc" file to the root of your project containing the following content:

```
registry=https://registry.npmjs.com/
@centrual:registry=https://npm.pkg.github.com
_authToken="YOUR_TOKEN"
email=your@email.address
always-auth=true
```

Then change `YOUR_TOKEN` with the newly created token and change `your@email.address` with your e-mail address

Now you can install the package to your project:

`npm i @centrual/geyt_api_client` or `yarn add @centrual/geyt_api_client`

Voilà! 🎉

Good job 🙏
