 # webpack.config.js
 
 ## Top Level

| Variables | Use                                                              | Example                                                                           |
| --------- | ---------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| entry     | entry point for webpack                                          | `./js/root/Index.js  `                                                             |
| output    | output location for packed files                                 | `filename: '[name].[contenthash]`[^2]`.js',  path: path.resolve(__dirname, 'dist')`[^1] |
| mode      | developer or production                                          | `mode: 'development'  `                                                             |
| module    | container for module settings                                    |                                                                                   |
| rules     | container in module that allows for setting up of per file rules |                                                                                   |
|           |                                                                  |                                                                                   |

## Module : Rules
### Example
![[Pasted image 20210810102504.png]]

Module rules for loading of Javascript .js files using babel-loader with preset-env preset and three plugins

### Table

| Variable      | Use                                                      |
| ------------- | -------------------------------------------------------- |
| test          | Regex test of a file name                                |
| loader or use | Load files that match the regex test using these loaders |
| exclude       | Do not load files from this directory                    |
| options       | additional options                                       |
| presets       | loader presets                                           |
| plugins       | extra loader plugins to use                                                         |


[^1]: path.resolve is a function that gets the local path on the machine so you do not need to specifiy it

[^2]: [contenthash] is the cache busting keyword, it appends a hash of the content to the file name so that when it is changed it forces an update