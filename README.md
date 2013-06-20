workstation Cookbook
====================
Manages a workstation which resides behind a corporate firewall.

Requirements
------------
### Cookbooks
- `ntp` - uses ntp cookbook to manage ntp configuration
- `vagrant` - uses the vagrant cookbook to manage vagrant
- `virtualbox` - uses the VirtualBox cookbook to manage Oracle
  VirtualBox installs.

### Platforms
The following platforms are going to be supported in this order:

- `CentOS` - 6.4
- `MacOS` - 10.7
- `Windows` - Not yet... Want to volunteer?
- `RedHat` - Not yet... Want to volunteer?

Attributes
----------

#### workstation::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['workstation']['repos_to_delete']</tt></td>
    <td>String Array</td>
    <td>An array of default yum repositories to delete.</td>
    <td><tt>
	  /etc/yum.repos.d/CentOS-Base.repo,
      /etc/yum.repos.d/CentOS-Debuginfo.repo,
      /etc/yum.repos.d/CentOS-Media.repo,
     /etc/yum.repos.d/CentOS-Vault.repo
	</tt></td>
  </tr>
  <tr>
    <td><tt>['workstation']['packages']</tt></td>
    <td>String Array</td>
    <td>description</td>
    <td><pre>
   xorg-x11-drivers
   xorg-x11-server-Xorg
   xorg-x11-xauth
   xorg-x11-xinit
   NetworkManager
   NetworkManager-gnome
   abyssinica-fonts
   alsa-plugins-pulseaudio
   at-spi
   bind-utils
   control-center
   createrepo
   dejavu-fonts-common
   dejavu-sans-fonts
   dejavu-sans-mono-fonts
   dejavu-serif-fonts
   dbus
   firstboot
   gdm
   gdm-user-switch-applet
   glx-utils
   gnome-panel
   gnome-power-manager
   gnome-screensaver
   gnome-session
   gnome-terminal
   gvfs-archive
   gvfs-fuse
   gvfs-smb
   liberation-fonts-common
   liberation-mono-fonts
   liberation-sans-fonts
   liberation-serif-fonts
   metacity
   nautilus
   notification-daemon
   polkit-gnome
   rdesktop
   traceroute
   tsclient
   xdg-user-dirs-gtk
   xorg-x11-fonts-100dpi
   xorg-x11-fonts-ISO8859-1-100dpi
   xorg-x11-fonts-Type1
   xorg-x11-fonts-misc
   xorg-x11-server-utils
   xorg-x11-utils
   xterm
   xvattr
   wdaemon
   yelp
   yum-utils
   man
   man-pages
   evolution
   evolution-exchange
   evolution-mapi
   firefox
   eclipse-platform
   eclipse-jdt
   emacs
   emacs-git
   gcc
   git
   livecd-tools
   rpm-build
   syslinux
	</pre></td>
  </tr>
}
</table>

Usage
-----
#### workstation::default
Just include `workstation` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[workstation]"
  ]
}
```

Contributing
------------

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write you change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: Paul Brown

