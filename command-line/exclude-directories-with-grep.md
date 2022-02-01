# Exclude Directories with Grep

I keep doing a recursive grep (`-r`) and it takes a long time because it searches dependency folders such as `node_modules`.

To exclude a directory, use `--exclude-dir=<dirname>`. This will apply recursively too, so:

`grep -r --exclude-dir=node_modules 'a-search-term' .`

Will perform a recursive directory search from the current directory, for 'a-search-term', excluding any directories named `node_modules`. Multiple `--exclude-dir` flags can be set to exclude other directories too.
