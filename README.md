# hello.nrfcloud.com CI

Uses [bifravst/ci](https://github.com/bifravst/ci) to set up the permissions in our AWS CI account for the repositories in this
GitHub organization that are supposed to have access so they are be able to use
it for CI runs.

The allowed list of repositories is managed via the [`repos.txt`](./repos.txt)
file.

> [!CAUTION]  
> Do not run this against the production account, but against the CI account.

```bash
git clone https://github.com/bifravst/ci
npm ci
STACK_NAME=bifravst-ci REPOS_LIST=../repos.txt npx cdk deploy
```
