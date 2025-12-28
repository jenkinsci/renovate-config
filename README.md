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

Before committing, install [NodeJS](https://nodejs.org/en/download) (or use [Node Version Manager](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating))  then run:

```sh
npx --yes --package renovate -- renovate-config-validator --strict
```

This triggers the [config validation](https://docs.renovatebot.com/config-validation/) to ensure the configuration is valid.

## References

- [Renovate Documentation](https://docs.renovatebot.com/)
