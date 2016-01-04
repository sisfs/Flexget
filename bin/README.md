# Supporting Python Scripts

I have really only modified the [deluge_torrent_complete](https://github.com/sisfs/dotfiles/blob/adding-my-changes/bin/deluge_torrent_complete) file for use with the Deluge [execute](http://dev.deluge-torrent.org/wiki/Plugins/Execute) plugin.

My situation my be different from yours but, in my case execute is called as follows: 

### In Deluge>Preferences>Execute>Torrent Complete:

/usr/local/bin/python2.7 /home/deluge/.flexget/bin/deluge_torrent_complete

## Issues

## Currently the deluge execute plugin is not actually running the script. I can run it from CLI (with errors) but deluge does not seem to be calling it at all. I have also added a deluge_torrent_added bash script that doesnt seem to be getting called either.

I am wondering if this issue is based on my running under FreeBSD or possibly missing a dependency somewhere that is not apparent to me.  
I tried to connect to the deluge git repo to check for dependencies but cannot connect.  
  
### More to Follow!
