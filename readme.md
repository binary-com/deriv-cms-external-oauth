# Deriv Netlify CMS external OAuth

This repo contains the `Vercel Serverless Functions` as `OAuth` providers for `deriv-api-docs` netlify-cms login with github.

## Prerequisites

Please make sure you read through [vercel serverless functions](https://vercel.com/docs/concepts/functions/serverless-functions) documentations.

## Instructions

In the `Settings` section in vercel please add these `ENVIRONMENT_VARIABLES` , filling in `OAUTH_CLIENT_ID` and
`OAUTH_CLIENT_SECRET` with your GitHub OAuth app's ID and secret. Also ensure that your GitHub OAuth app's
callback URL matches `COMPLETE_URL`.

```text
DEBUG=netlify-cms-oauth-provider-node*
COMPLETE_URL=http://some-domain-generated-by-vercel.vercel.app/api/complete
OAUTH_CLIENT_ID=github app client id
OAUTH_CLIENT_SECRET=github app client secret
NODE_ENV=development if you want to see verbose logs
OAUTH_PROVIDER=github
ORIGIN=the actual domain of the project deployment (for example : api.deriv.com )
```
