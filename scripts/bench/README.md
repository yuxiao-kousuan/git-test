# React Benchmarking

## Commands

In most cases, the only two commands you might want to use are:

- `yarn start`
- `yarn --cwd=../../ build react/index,react-dom/index --type=UMD_PROD && yarn start --skip-build`


The second command will run all benchmarks but skip the build process. This is useful for when doing local performance tweaking and the remote repo has already had its bundles built. Both local and remote repos will be run against all benchmarks with this command too. abc

这是修改的内容

这是修改的内容2


# will compare local repo vs remote merge base repo
yarn start

# will compare local repo vs remote merge base repo
# this can significantly improve bench times due to no build
yarn start --skip-build

# will only build and run local repo against benchmarks (no remote values will be shown)
yarn start --local

# will only build and run remote merge base repo against benchmarks (no local values will be shown)
yarn start --remote

# will only build and run remote main repo against benchmarks
yarn start --remote=main

# same as "yarn start"
yarn start --remote --local

# runs benchmarks with Chrome in headless mode
yarn start --headless

# runs only specific string matching benchmarks
yarn start --benchmark=hacker

