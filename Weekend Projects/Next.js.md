# Learning New Things~

<br/>

## Tooling
- [next.js](https://nextjs.org/docs/getting-started)
- [emotion](https://emotion.sh/docs/introduction)
- [sanity](https://www.sanity.io/docs/graphql)
- [apollo](https://www.apollographql.com/docs/apollo-server/deployment/netlify/)

## What're we gonna build?

**Rebuilding the BLMLondon website in NextJS


## Steps:
1. set up monorepo
	- `mkdir blmlondon-next && cd blmlondon-next`
	- `yarn init`
		```
		question name (blmlondon-next): 
		question version (1.0.0): 
		question description: 
		question entry point (index.js): 
		question repository url: 
		question author: Alex Low
		question license (MIT): 
		question private: true

		```
	- edit `package.json` in root folder to look like this:
		```json
		{
		  "name": "blmlondon-next",
		  "version": "1.0.0",
		  "description": "BLMLondon website",
		  "main": "index.js",
		  "author": "Alex Low",
		  "license": "MIT",
		  "private": true,
		  "workspaces": [
			"site",
			"sanity"
		  ]
		}
		```
	- `yarn create next-app site`
	- `cd site && rm -rf .git`
	- `cd ..`
	- `touch .gitignore`
		- add `node_modules/` to `.gitignore`
	- `touch README.md`
		- I'm a big fan of adding a `:^ )` for my baby brain lorem
	- `mkdir sanity && cd sanity && sanity init`
		- follow along with initial setup. Pick the `Blog` starter schema
		- modify name of `package.json` in `/sanity` to be `sanity`
	- cd back up to the root folder of the project
	- setup a new [github](https://github.com/) repo. In this case, I'm going with `blmlondon-next`
	- I went through the standard affair initiating my repo:
		```
		git init
		git add .
		git commit -m"first commit"
		git remote add origin https://github.com/XanderJL/blmlondon-next.git
		git push -u origin master
		```
	- next, we'll set up a `develop` branch
	- `git checkout -b develop`
	- `git push -u origin develop`
	- onto the fun part!
1. Guess we should set up Apollo for our data layer
	- 
2. spin up dev server
	- `yarn workspace site dev`
		- your local server should have spun up on http://localhost:3000