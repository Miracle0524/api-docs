# Worth API docs

**Description**

Steps to run project locally

> ⚠️ **Prerequisite:** Please install Node.js (version 21 or higher) before proceeding.

If you are using a Node.js version earlier than 21, please follow these below steps. Otherwise, you can directly proceed to the installation instructions.

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

Execute the following command to run the mintlify project locally:

> ⚠️ **Warning:** Ensure that you are in the root directory of your `mint.json` file.

```
mintlify dev
```

Mintlify by default runs at port `3000`, so local preview of it can be found at `http://localhost:3000`

You can customize the port Mintlify runs on by using the `--port` flag. To run Mintlify on port 3333, for instance, use this command:

```
mintlify dev --port 3333
```

### API Endpoints

To add your own api endpoints use below command:

```
npx @mintlify/scraping@latest openapi-file <path-of-openapi-json-file> -o <path-to-folder-to-extract-json-file-data>
```

For example:
```
npx @mintlify/scraping@latest openapi-file openapi/file -o api-reference/folder
```

## Summary
Now you're all set towork with Mintlify locally. Happy coding!
