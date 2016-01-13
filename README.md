# [Flexget](http://www.flexget.com) Configuration Files

Created by: [Jeff Wilson](mailto:jeff@jeffalwilson.com)  
Original Available from: (https://github.com/jawilson/dotfiles)

Forked by: [Matt Tallant](mailto:m.tallant+github@gmail.com)  
This Fork is available at: (https://github.com/sisfs/dotfiles)

Forked by: [Russ King](mailto:russelltking@gmail.com)  
This Fork is available at: (https://github.com/sarethan/Flexget)

I am really only interested in the FlexGet config portion of this dotfiles fork and have removed a lot of the other files...

### Installation Instructions ###

    git clone https://github.com/sarethan/Flexget.git ~/.flexget
    
### You can set up links to files from here instead of overwriting your .flexget directory before you're prepared. ###

    mv ~/.flexget/config.yml ~/.flexget/old-config.yml
    ln ~/.flexfiles/config.yml ~/.flexget/config.yml 

### DDNS Setup ###
    
    [DuckDNS](https://www.duckdns.org/install.jsp?tab=linux-cron&domain=small)
    
## Secrets Plugin ##

I'm using the [secrets](http://flexget.com/wiki/Plugins/secrets) plugin to hide my private credentials for various plugins. If you want to do this as well, you will need to create a ``secretfile.yml`` file in the same directory as your ``config.yml``.


This entire setup should result in a single video file (``.mkv``, ``.mp4``, etc) in the final destination with a nice name

Here's the gist of how it works:
  1. Flexget accepts the torrent
  2. The torrent is added to Deluge 
  7. ``deluge_torrent_complete`` calls flexget with a completely separate config, ``sorting.yml`` ([also available in this repository](https://github.com/sisfs/dotfiles/blob/master/flexget/sorting.yml))
  8. 
  9. ``deluge_torrent_complete`` tells my [Plex Media Server](https://plex.tv/) to [update the library](http://forums.plex.tv/discussion/comment/372419/#Comment_372419) (scan for new files)
