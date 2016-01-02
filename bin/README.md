# Supporting Python Scripts

I have really only modified the [deluge_torrent_complete](https://github.com/sisfs/dotfiles/blob/adding-my-changes/bin/deluge_torrent_complete) file for use with the Deluge [execute](http://dev.deluge-torrent.org/wiki/Plugins/Execute) plugin.

My situation my be different from yours but, in my case execute is called as follows: 

### In Deluge>Preferences>Execute>Torrent Complete:

/usr/local/bin/python2.7 /home/deluge/.flexget/bin/deluge_torrent_complete

## Issues

I am having trouble currently knowing that the plugin is working on those torrents not containing .rar files.

To combat this I am trying to get the Python script to add logging when it works right but this is my first foray into python =(
### More to Follow!
