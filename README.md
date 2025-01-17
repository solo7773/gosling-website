# A Documentation Website for Gosling.js

This website is built using [Docusaurus 2](https://v2.docusaurus.io/), a modern static website generator.


## Installation

```sh
yarn install
```

## Local Development


```sh
yarn start
```

The above command starts a local development server and open up a browser window. Most changes are reflected live without having to restart the server.


Gosling uses `assets/gosling.schema.json` to generate property tables.  
If you have a local `gosling.js` repo and want to update the gosling.schema from that repo.  
Assuming your `gosling-website` and `gosling.js` repos are in the same directory, you can run
```
cd assets
. copy.sh
```

## Build

```sh
yarn build
```

The above command generates static content into the `build` directory and can be served using any static contents hosting service.

## Deployment

```console
GIT_USER=<Your GitHub username> USE_SSH=true yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.

## Tagging a new version

```
yarn run tag_version x.x.x
```

This command will:
- Copy the full docs/ folder contents into a new versioned_docs/version-<x.x.x>/ folder.
- Create a versioned sidebars file based from your current sidebar configuration (if it exists) - saved as versioned_sidebars/version-<x.x.x>-sidebars.json.
- Append the new version number to versions.json.