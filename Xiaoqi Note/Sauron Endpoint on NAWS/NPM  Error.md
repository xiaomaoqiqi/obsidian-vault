---
created: 2022-09-09T14:01:08-04:00
updated: 2022-09-09T14:01:08-04:00
---

Issue: 

npm WARN lifecycle The node binary used for scripts is /Users/xiaoqipm/xiaoqiNAWS/env/CDKBuild-2.x/runtime/bin/node but npm is using /opt/homebrew/Cellar/node@12/12.22.12_1/bin/node itself. Use the `--scripts-prepend-node-path` option to include the path for the node binary npm was executed with.


`npm` is complaining because the location of `npm` and `node` don't match up. `npm` is coming from a PATH inside a Brazil package, but `node` is coming from a version installed directly in the system. This is a little wonky, and could lead to either failures or works-on-my-box-fails-in-build-fleet problems. (More likely if the versions don't match up)

`npm` itself already has a `scripts-prepend-node-path` configuration to avoid this mismatch.

-   [https://docs.npmjs.com/cli/v6/commands/npm-run-script](https://docs.npmjs.com/cli/v6/commands/npm-run-script)
-   [https://stackoverflow.com/questions/51293566/how-to-include-the-path-for-the-node-binary-npm-was-executed-with](https://stackoverflow.com/questions/51293566/how-to-include-the-path-for-the-node-binary-npm-was-executed-with)

#### If you want to set `scripts-prepend-node-path` for your machine

Run this command.

```
npm config set scripts-prepend-node-path true
```

This applies to all your workspaces/packages/etc. Co-workers may also need to do this. If you use `n` or similar to manage multiple versions of `npm` you might need to set it for each.

If you need to **undo** the configuration:

```
npm config delete scripts-prepend-node-path
```

#### If you want to set `scripts-prepend-node-path` for the package

Add this line to an `.npmrc` file in your package root.

```
scripts-prepend-node-path=true
```

If you need to **undo** the configuration, remove the line.

This applies to the package. Co-workers will get the change, it won't matter if you switch to different versions of `npm` with `n` or similar. Other packages, even in the same workspace, will still have warnings and may use a different `node` for local development.











