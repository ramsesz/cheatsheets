# cheatsheets
kleine scriptjes die alles vergemakkelijken

## php

### xdebug

to enable CLI xdebug debugging
export XDEBUG_CONFIG="remote_enable=1 remote_mode=req remote_port=9900 remote_host=127.0.0.1 remote_connect_back=0"

## unix systems (linux/osx)

##### currentdate
$(date +'%Y%m%d%H%M%S')

##### flatten folder
find /source -type f -exec mv --backup=numbered -t /destination {} +


### wp-cli
wp db export ./filename.$(date +'%Y%m%d%H%M%S’).sql



### Other cheatsheets
[Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
