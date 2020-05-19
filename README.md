Move - Near
==========

[![Build Status](https://travis-ci.com/near-examples/guest-book.svg?branch=master)](https://travis-ci.com/near-examples/guest-book)

Demo Video Link: https://vimeo.com/420360884

Move-Near is an application powered by the NEAR Protocol that helps bring Financial and Social Inclusion. One of the major problems it solves is that of travel during this world-wide pandemic. With inputs from the local goverment I have created a system which allows everyone to travel with a Pass issued. This would stop useless travel and help prevent further spread of Coronoavirus. This systems signitficantly brings in transparency to the entire centralized system. 
Move-Near is also a platform where people can easily create DAOs and Campaigns for fundraising in just few clicks. People from all around the globe can contirbute towards it. There is also an option to get the DAO verified which increases the chance of more funding. However, it is not a must. The sytem is robust enough to support the Scheme and Stimulus Package distribution which will ease the work a lot. 

With Move-Near we are bringing in Social and Financial inclusion in a decentralized way. 

Shout out to the Amazing NEAR team for helping me in building this application. There are tons of things I have learnt and possible have some ideas for more contribution to the NEAR community.

Below are the steps to start the application.

Quick Start
===========

To run this project locally:

1. Prerequisites: Make sure you have node.js installed (we like [asdf] for
   this), then use it to install [yarn]: `npm install --global yarn` (or just
   `npm i -g yarn`)
2. Install dependencies: `yarn install` (or just `yarn`)
3. Run the local development server: `yarn dev` (see `package.json` for a
   full list of `scripts` you can run with `yarn`)

Now you'll have a local development environment backed by the NEAR TestNet! Running `yarn dev` will tell you the URL you can visit in your browser to see the app.


Exploring The Code
==================

1. The backend code lives in the `/assembly` folder. This code gets deployed to
   the NEAR blockchain when you run `yarn deploy:contract`. This sort of
   code-that-runs-on-a-blockchain is called a "smart contract" – [learn more
   about NEAR smart contracts][smart contract docs].
2. The frontend code lives in the `/src` folder.
   [/src/index.html](/src/index.html) is a great place to start exploring. Note
   that it loads in `/src/index.js`, where you can learn how the frontend
   connects to the NEAR blockchain.
3. Tests: there are different kinds of tests for the frontend and backend. The
   backend code gets tested with the [asp] command for running the backend
   AssemblyScript tests, and [jest] for running frontend tests. You can run
   both of these at once with `yarn test`.

Both contract and client-side code will auto-reload as you change source files.


Deploy
======

Every smart contract in NEAR has its [own associated account][NEAR accounts]. When you run `yarn dev`, your smart contracts get deployed to the live NEAR TestNet with a throwaway account. When you're ready to make it permanent, here's how.


Step 0: Install near-shell
--------------------------

You need near-shell installed globally. Here's how:

    npm install --global near-shell

This will give you the `near` [CLI] tool. Ensure that it's installed with:

    near --version


Step 1: Create an account for the contract
------------------------------------------

Visit [NEAR Wallet] and make a new account. You'll be deploying these smart contracts to this new account.

Now authorize NEAR shell for this new account, and follow the instructions it gives you:

    near login


Step 2: set contract name in code
---------------------------------

Modify the line in `src/config.js` that sets the account name of the contract. Set it to the account id you used above.

    const CONTRACT_NAME = process.env.CONTRACT_NAME || 'your-account-here!'


Step 3: deploy!
---------------

One command:

    yarn deploy

As you can see in `package.json`, this does two things:

1. builds & deploys smart contracts to NEAR TestNet
2. builds & deploys frontend code to GitHub using [gh-pages]. This will only work if the project already has a repository set up on GitHub. Feel free to modify the `deploy` script in `package.json` to deploy elsewhere.



  [NEAR]: https://nearprotocol.com/
  [asdf]: https://github.com/asdf-vm/asdf
  [yarn]: https://yarnpkg.com/
  [AssemblyScript]: https://docs.assemblyscript.org/
  [React]: https://reactjs.org
  [smart contract docs]: https://docs.nearprotocol.com/docs/roles/developer/contracts/assemblyscript
  [asp]: https://www.npmjs.com/package/@as-pect/cli
  [jest]: https://jestjs.io/
  [NEAR accounts]: https://docs.nearprotocol.com/docs/concepts/account
  [NEAR Wallet]: https://wallet.nearprotocol.com
  [near-shell]: https://github.com/nearprotocol/near-shell
  [CLI]: https://www.w3schools.com/whatis/whatis_cli.asp
  [create-near-app]: https://github.com/nearprotocol/create-near-app
  [gh-pages]: https://github.com/tschaub/gh-pages
