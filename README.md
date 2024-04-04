# whatsapp-web.js BluePepper's custom version

## Original repository

See [the original repo](https://github.com/pedroslopez/whatsapp-web.js).

## Installation

The module is available on github packages.
[Whatsapp productivity](https://github.com/bluepepperok/whatsapp-productivity) has a dependency on this library. It's `package.json` includes: `"@bluepepperok/whatsapp-web.js": "^specificVersionToUse"`.

## New versions
- If you want to start off a different branch of the original repo, create a new branch with the content of that branch.
- Before making any changes, update the `version` field on [package.json](package.json) to `originalVersion-bp-N-dev` and commit the file to git. N starts with 1 and should be increased for every custom version based off the same original version.  
- See the changes already done by BluePepper on other branches of this project and check whether you need to cherry pick some commits.
- Make the changes you want.
- Use [example.js](example.js) to test your changes.
- Make "Whatsapp productivity" use your local version of this library and test the changes.
  - Get "Whatsapp productivity" use your local version of this library  
    - Update "Whatsapp productivity"'s `package.json` to use `@bluepepperok/whatsapp-web.js": "file:/pathToBaseDirWhereYouCloneGithubRepos/whatsapp-web.js` and run `npm install`.
     - Alternatively you could use `npm link` on whatsapp-web.js dir and then `npm link @bluepepperok/whatsapp-web.js` on "Whatsapp productivity" dir
  - If whatsapp-web.js changed its dependencies, make sure you are testing "Whatsapp productivity" with the updated dependencies.
  - Test the changes
- Update the `version` field on [package.json](package.json) to `originalVersion-bp-N` and commit the file to git.
- To publish a package version you need your own `.npmrc` (See `.npmrc.example`)
- `npm publish`
- Make sure the package was published on the packages section of this repo.
- Update "Whatsapp productivity"'s `package.json` to use the new version of this library and test the changes.


## How to get the .npmrc authToken / YOUR_PERSONAL_ACCESS_TOKEN
- Login to github
- Go to https://github.com/settings/tokens
- Click "generate new token"
- Choose the "classic" token mode
- Set the title and expiration date you want
- On the scope section, check `read:packages`, `write:packages`, `delete:packages` and `repo` 
- Click "generate token".
