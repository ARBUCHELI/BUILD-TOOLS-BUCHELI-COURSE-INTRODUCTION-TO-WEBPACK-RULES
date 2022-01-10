# BUILD-TOOLS-BUCHELI-COURSE-INTRODUCTION-TO-WEBPACK-RULES

Webpack uses rules to know what to do with different file types. Webpack expects an array of rules in a configuration option called module. The syntax looks like:

```
module.exports = 
{
  module: 
  {
    rules: []
  }
}
```

A rule has a test configuration option defined as a regular expression. If a file matches the regular expression, Webpack will use the rule on that file. For example, if we 
define test as \.txt$\i, the rule will apply to files ending in .txt.

The other part of the rule needs to tell Webpack what to do with files that match the test. That part of the rule varies by file type.

For .txt files, the rule inside of rules would look like:

```
rules: 
[
  {
    test: /\.txt$/i,
    type: 'asset/source'
  }
]
```

We would first run the build command in one terminal, to create the bundle and wait for updates.

npm run build

We would next launch a second terminal and run the start command to serve the site.

npm run start
