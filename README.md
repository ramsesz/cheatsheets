# [RAMSESZ](https://www.ramsesz.be) cheatsheets
little small scripts I use a lot during development
https://www.ramsesz.be


## UNIX systems (linux/osx)
##### currentdate
_current date  shell variable_
```shell
$(date +'%Y%m%d%H%M%S')
```
##### flatten folder
flatten subdirectories recursively to destination
```shell
find /source -type f -exec mv --backup=numbered -t /destination {} +
```
##### tar directory
tars and gzips directory
```shell
tar -zcvf archive-name.tar.gz [directory-path]
```
##### find how many inodes in current directory
inodes in curren directory
```shell
find . -printf '%i\n' | sort -u | wc -l
```
##### Find biggest directories / files
_directories_
```shell
du -a ./(path) | sort -n -r | head -n 10

# current directory
du -a . | sort -n -r | head -n 10
```
_files_
```shell
# Warning: only works with GNU find
find /path/to/dir/ -printf '%s %p\n'| sort -nr | head -10

# current directory
find . -printf '%s %p\n'| sort -nr | head -10
```



## Wordpress
### [wp-cli](http://wp-cli.org)
export database with current date in filename
```shell
wp db export ./filename.$(date +'%Y%m%d%H%M%S').sql
```
search-replace domain
for more options and examples
http://wp-cli.org/commands/search-replace/

```shell
# single blo
wp search-replace 'http://www.source.be' ‚'http://www.target.be'

# multisite all network
wp search-replace 'http://www.source.be' ‚'http://www.target.be' --network

# multisite all network
# example.com is site which should be replaced for these columns (wp_options wp_blogs)
wp search-replace --url=example.com example.com example.dev 'wp_*options' wp_blogs
```


## PHP
### xdebug

_enable CLI xdebug debugging from cli_
```shell
export XDEBUG_CONFIG="remote_enable=1 remote_mode=req remote_port=9900 remote_host=127.0.0.1 remote_connect_back=0"
```



## Other cheatsheets
[Markdown cheatsheet](https:#github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
