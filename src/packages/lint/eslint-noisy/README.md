## about package name
i named this package `noisy` is because the other eslint plugins for fis all silently failed when error report by eslint.

## usage
```
// fis-conf.js

var eslintConf = {};

fis.match('*.js', {
  lint: fis.plugin('eslint-noisy', eslintConf)
});
```

### options

options: [http://eslint.org/docs/developer-guide/nodejs-api#cliengine]

rules and fixable rules: [http://eslint.org/docs/rules/]

```
var eslintConf = {
  configFile:
  envs: // default: ['browser']
  extensions:
  globals:
  fix: , // ❗!!! important !!!❗
         // default:false,
         // be careful, this might change your source code
         // this will trigger `CLIEngine.outputFixes` automatically
  ignore:
  ignorePath:
  ignorePattern:
  baseConfig:
  rulePaths:
  rules:
  useEslintrc: // defalut: true
  parser:
  cache:
  cacheFile:
  cacheLocation:
  cwd:
};
```
