### Contributing Guide 

## Warning

We are currently in the process of ironing out the legal stuff regarding doing our very first (strategic) open source project.

In particular we are still missing a contributor license agreement and automatic tooling to make sure PRs sign it.

If you would like to contribute in the meantime please contact us (benji@testim.io / bnaya@testim.io) directly.



## Technical Know-How

This monorepo is managed with yarn workspaces in order to build it:

```shell
# install dependencies
yarn
# run a package, for example the tester
cd packages/jest-tester-and-example
yarn test
```

Because the project is still pretty early if you want to contribute  but unsure how please contact us.

Pleae note our code of conduct. We take it seriously and we value diverse contributions and have a zero tolerance policy towards discrimination of any kind.


## Publish workflow

We use lerna for publishing.

We use [lerna canary publish](https://github.com/lerna/lerna/tree/master/commands/publish#--canary) for PRs.  

To release prod packages, we use [lerna from-git workflow](https://github.com/lerna/lerna/tree/master/commands/publish#bump-from-git).  
You need to run `lerna version` locally on master branch. it will create version commit, tags and push it to the git remote

Our versioning strategy is `dependent` and not `independent`. means all of the released packages will have the same version.

### We are not semver compatible yet! keep version number below 1.0

For all the other details, look at [.circleci/config.yml](.circleci/config.yml)
