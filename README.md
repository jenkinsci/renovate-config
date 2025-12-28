# renovate-config

This repository contains a custom configuration preset for Jenkins plugins.

## Usage
1. Check to see if you have a `renovate.json` already. It can be in any of these [possible locations](https://docs.renovatebot.com/getting-started/installing-onboarding/#configuration-location).

We recommend moving it to `.github/renovate.json` if it is not already there.

2. Change `renovate` config to:

    ```json5
    {
      "$schema": "https://docs.renovatebot.com/renovate-schema.json",
      "extends": [
        "github>jenkinsci/renovate-config"
      ]
    }
    ```
3. That's it. Renovate will now use the custom configuration preset.

## Development

When contributing to this repository, validate your local changes running the following snippet:

```sh
npm install
npm test
```

This triggers the [config validation](https://docs.renovatebot.com/config-validation/) to ensure the configuration is valid.

## Validating your own `renovate.json`

If you want to validate `.github/renovate.json` in your repository, you can execute the following command.  
Make sure to install [NodeJS](https://nodejs.org/en/download) (or use [Node Version Manager](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating)) then run:

```sh
npx --yes --package renovate -- renovate-config-validator --strict
```

# References

- [Renovate Documentation](https://docs.renovatebot.com/)
