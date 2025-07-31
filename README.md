# Worth API docs

**Description**

Steps to run project locally

> ⚠️ **Prerequisite:** Your local node version must be 21.0.0 to run Mintlify docs locally. Versions higher or lower than this are not supported.

If you are using a Node.js version other than 21.0.0, please follow these below steps. Otherwise, you can directly proceed to the installation instructions.

1. Install nvm
2. Run command
```
nvm install 21.0.0
```
3. After installation use
```
nvm use 21.0.0
```
4. Check node version with ```node -v```

If you see `21.0.0`, you are good to go!

## Installation

Download the Mintlify CLI using the following command
```
npm i mintlify -g
```

Check if mintlify is installed or not using ```mintlify -v```

After installing Mintlify, you can proceed to the next step.

## Development

Support link: [Mintlify Confluence Documentation](https://worth-ai.atlassian.net/wiki/spaces/joinworth/pages/170229767/Mintlify+API+Docs...)

Execute the following command to run the mintlify project locally:

> ⚠️ **Warning:** Ensure that you are in the root directory of your `mint.json` file.

```
mintlify dev
```

By default, Mintlify deploys to port `3000`, so a local preview may be found at `http://localhost:3000`. If port `3000` is not available when deploying locally, mintlify will iterate the port number by 1 until it finds an available port to deploy to.

You can customize the port Mintlify runs on by using the `--port` flag. To run Mintlify on port `3333`, for instance, use the command:

```
mintlify dev --port 3333
```

### API Endpoints
It is important to understand that these docs were first generated using Mintlify's automated tool that scrapes our API endpoints to produce schemas and output examples. While this worked to establish an initial structure, its results were inaccurate and confusing to users. Since then, numerous manual changes have been made (and are continuing to be made) to improve accuracy and readability of our API documentation. Please rely on manual changes rather than using the automated scraping tool as the latter may automatically overwrite our documentation with informationt that is inaccurate and/or confusing.

To add your own api endpoints use below command. Please do NOT overwrite existing api endpoints.

```
npx @mintlify/scraping@latest openapi-file <path-of-openapi-json-file-with-extension> -o <path-to-folder-to-extract-json-file-data>
```

For example:
```
npx @mintlify/scraping@latest openapi-file openapi/file.json -o api-reference/folder
```

## Summary
Now you're all set to work with Mintlify locally. Happy coding!
