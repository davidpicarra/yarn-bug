# yarn-bug

## [Yarn issue #3333](https://github.com/yarnpkg/yarn/issues/3333)

**Do you want to request a *feature* or report a *bug*?**
Reporting a bug

**What is the current behavior?**
Repository created to show this bug: https://github.com/davidpicarra/yarn-bug

1. have a ```package.json``` with a dependency where the key is different than the name inside the imported dependency, for example:
```"fake-vue": "git+https://github.com/vuejs/vue.git#b977c77"```
2. execute ```yarn```
3. check ```node_modules/fake-vue``` exists and ```node_modules/vue``` doesn't exist
4. delete ```node_modules```
5. execute ```npm install```
6. check only ```node_modules/vue``` exists

**What is the expected behavior?**
It should generate the same folder output in both cases, was expecting the folder ```node_modules/vue``` to exist when installing packages via ```yarn```

**Please mention your node.js, yarn and operating system version.**
→ yarn --version
0.23.4

→ node --version
v7.10.0

→ npm --version
4.2.0

macOS Sierra 10.12.4