# Serverless Action

GitHub Action to deploy with Serverless

## Install

To use this action insure that `package.json` has the script `deploy` setup e.g.

```bash

    "scripts": {
        ...
        "deploy": "serverless deploy"
    }

```

## Usage

```bash

    deploy-frontend:
        name: Deploy
        runs-on: ubuntu-latest
        steps:
          - name: Checkout Code
              uses: actions/checkout@v2

          - name: Backend
              uses: clockwork-marketing-uk/actions-serverless@1.0.0
              with:
                environment: "production"
                account_id: "12345"
                region: "eu-west-2"
                working-directory: ./back-end

```
