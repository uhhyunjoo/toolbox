### neofetch

```
 sudo apt update
```

```
sudo apt install neofetch
```

```
neofetch
```

```
(torch) hjlee@befb64e1d467:~/workspace/Github/pytorch-lightning$ neofetch
            .-/+oossssoo+/-.               hjlee@befb64e1d467 
        `:+ssssssssssssssssss+:`           ------------------ 
      -+ssssssssssssssssssyyssss+-         OS: Ubuntu 18.04.5 LTS x86_64 
    .ossssssssssssssssssdMMMNysssso.       Host: DGX-1 with V100-32 v1.0 
   /ssssssssssshdmmNNmmyNMMMMhssssss/      Kernel: 4.15.0-39-generic 
  +ssssssssshmydMMMMMMMNddddyssssssss+     Uptime: 88 days, 4 hours, 23 mins 
 /sssssssshNMMMyhhyyyyhmNMMMNhssssssss/    Packages: 326 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Shell: bash 4.4.20 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   CPU: Intel Xeon E5-2698 v4 (80) @ 3.600GHz 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   Memory: 105564MiB / 515883MiB 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+                           
.ssssssssdMMMNhsssssssssshNMMMdssssssss. 
 /sssssssshNMMMyhhyyyyhdNMMMNhssssssss/ 
  +sssssssssdmydMMMMMMMMddddyssssssss+ 
   /ssssssssssshdmNNNNmyNMMMMhssssss/ 
    .ossssssssssssssssssdMMMNysssso. 
      -+sssssssssssssssssyyyssss+- 
        `:+ssssssssssssssssss+:` 
            .-/+oossssoo+/-. 
```

![image](https://user-images.githubusercontent.com/41139770/168582626-54ca455b-43a9-4a8c-ad0a-41bdbb9df054.png)

```
(torch) hjlee@befb64e1d467:~/workspace$ neofetch --help
Usage: neofetch --option "value" --option "value"

Neofetch is a CLI system information tool written in BASH. Neofetch
displays information about your system next to an image, your OS logo,
or any ASCII file of your choice.

NOTE: Every launch flag has a config option.

Options:

INFO:
    --disable infoname          Allows you to disable an info line from appearing
                                in the output.

                                NOTE: You can supply multiple args. eg. 'neofetch --disable cpu gpu'

    --os_arch on/off            Hide/Show OS architecture.
    --speed_type type           Change the type of cpu speed to display.
                                Possible values: current, min, max, bios,
                                scaling_current, scaling_min, scaling_max

                                NOTE: This only supports Linux with cpufreq.

    --speed_shorthand on/off    Whether or not to show decimals in CPU speed.

                                NOTE: This flag is not supported in systems with CPU speed less than
                                1 GHz.

    --cpu_brand on/off          Enable/Disable CPU brand in output.
    --cpu_cores type            Whether or not to display the number of CPU cores
                                Possible values: logical, physical, off

                                NOTE: 'physical' doesn't work on BSD.

    --cpu_speed on/off          Hide/Show cpu speed.
    --cpu_temp C/F/off          Hide/Show cpu temperature.

                                NOTE: This only works on Linux and BSD.

                                NOTE: For FreeBSD and NetBSD-based systems, you need to enable
                                coretemp kernel module. This only supports newer Intel processors.

    --distro_shorthand on/off   Shorten the output of distro (tiny, on, off)

                                NOTE: This option won't work in Windows (Cygwin)

    --kernel_shorthand on/off   Shorten the output of kernel

                                NOTE: This option won't work in BSDs (except PacBSD and PC-BSD)

    --uptime_shorthand on/off   Shorten the output of uptime (tiny, on, off)
    --refresh_rate on/off       Whether to display the refresh rate of each monitor
                                Unsupported on Windows
    --gpu_brand on/off          Enable/Disable GPU brand in output. (AMD/NVIDIA/Intel)
    --gpu_type type             Which GPU to display. (all, dedicated, integrated)

                                NOTE: This only supports Linux.

    --gtk_shorthand on/off      Shorten output of gtk theme/icons
    --gtk2 on/off               Enable/Disable gtk2 theme/font/icons output
    --gtk3 on/off               Enable/Disable gtk3 theme/font/icons output
    --shell_path on/off         Enable/Disable showing $SHELL path
    --shell_version on/off      Enable/Disable showing $SHELL version
    --disk_show value           Which disks to display.
                                Possible values: '/', '/dev/sdXX', '/path/to/mount point'

                                NOTE: Multiple values can be given. (--disk_show '/' '/dev/sdc1')

    --disk_subtitle type        What information to append to the Disk subtitle.
                                Takes: name, mount, dir

                                'name' shows the disk's name (sda1, sda2, etc)

                                'mount' shows the disk's mount point (/, /mnt/Local Disk, etc)

                                'dir' shows the basename of the disks's path. (/, Local Disk, etc)

    --ip_host url               URL to query for public IP
    --song_shorthand on/off     Print the Artist/Title on separate lines
    --music_player player-name  Manually specify a player to use.
                                Available values are listed in the config file
    --install_time on/off       Enable/Disable showing the time in Install Date output.
    --install_time_format 12h/24h
                                Set time format in Install Date to be 12 hour or 24 hour.

TEXT FORMATTING:
    --colors x x x x x x        Changes the text colors in this order:
                                title, @, underline, subtitle, colon, info
    --underline on/off          Enable/Disable the underline.
    --underline_char char       Character to use when underlining title
    --bold on/off               Enable/Disable bold text

COLOR BLOCKS:
    --color_blocks on/off       Enable/Disable the color blocks
    --block_width num           Width of color blocks in spaces
    --block_height num          Height of color blocks in lines
    --block_range num num       Range of colors to print as blocks

BARS:
    --bar_char 'elapsed char' 'total char'
                                Characters to use when drawing bars.
    --bar_border on/off         Whether or not to surround the bar with '[]'
    --bar_length num            Length in spaces to make the bars.
    --bar_colors num num        Colors to make the bar.
                                Set in this order: elapsed, total
    --cpu_display mode          Bar mode.
                                Possible values: bar, infobar, barinfo, off
    --memory_display mode       Bar mode.
                                Possible values: bar, infobar, barinfo, off
    --battery_display mode      Bar mode.
                                Possible values: bar, infobar, barinfo, off
    --disk_display mode         Bar mode.
                                Possible values: bar, infobar, barinfo, off

IMAGE BACKEND:
    --backend backend           Which image backend to use.
                                Possible values: 'ascii', 'caca', 'catimg', 'jp2a', 'iterm2', 'off',
                                'sixel', 'tycat', 'w3m'
    --source source             Which image or ascii file to use.
                                Possible values: 'auto', 'ascii', 'wallpaper', '/path/to/img',
                                '/path/to/ascii', '/path/to/dir/'
    --ascii source              Shortcut to use 'ascii' backend.
    --caca source               Shortcut to use 'caca' backend.
    --catimg source             Shortcut to use 'catimg' backend.
    --iterm2 source             Shortcut to use 'iterm2' backend.
    --jp2a source               Shortcut to use 'jp2a' backend.
    --pixterm source            Shortcut to use 'pixterm' backend.
    --sixel source              Shortcut to use 'sixel' backend.
    --termpix source            Shortcut to use 'termpix' backend.
    --tycat source              Shortcut to use 'tycat' backend.
    --w3m source                Shortcut to use 'w3m' backend.
    --off                       Shortcut to use 'off' backend.

    NOTE: 'source; can be any of the following: 'auto', 'ascii', 'wallpaper', '/path/to/img',
    '/path/to/ascii', '/path/to/dir/'

ASCII:
    --ascii_colors x x x x x x  Colors to print the ascii art
    --ascii_distro distro       Which Distro's ascii art to print

                                NOTE: Arch and Ubuntu have 'old' logo variants.

                                NOTE: Use 'arch_old' or 'ubuntu_old' to use the old logos.

                                NOTE: Ubuntu has flavor variants.

                                NOTE: Change this to 'Lubuntu', 'Xubuntu', 'Ubuntu-GNOME',
                                'Ubuntu-Studio' or 'Ubuntu-Budgie' to use the flavors.

                                NOTE: Alpine, Arch, CRUX, Debian, Gentoo, FreeBSD, Mac, NixOS,
                                OpenBSD, and Void have a smaller logo variant.

                                NOTE: Use '{distro name}_small' to use the small variants.

    --ascii_bold on/off         Whether or not to bold the ascii logo.
    -L, --logo                  Hide the info text and only show the ascii logo.

                                Possible values: bar, infobar, barinfo, off

IMAGE:
    --loop                      Redraw the image constantly until Ctrl+C is used. This fixes issues
                                in some terminals emulators when using image mode.
    --size 00px | --size 00%    How to size the image.
                                Possible values: auto, 00px, 00%, none
    --crop_mode mode            Which crop mode to use
                                Takes the values: normal, fit, fill
    --crop_offset value         Change the crop offset for normal mode.
                                Possible values: northwest, north, northeast,
                                west, center, east, southwest, south, southeast

    --xoffset px                How close the image will be to the left edge of the
                                window. This only works with w3m.
    --yoffset px                How close the image will be to the top edge of the
                                window. This only works with w3m.
    --bg_color color            Background color to display behind transparent image.
                                This only works with w3m.
    --gap num                   Gap between image and text.

                                NOTE: --gap can take a negative value which will move the text
                                closer to the left side.

    --clean                     Delete cached files and thumbnails.

SCREENSHOT:
    -s, --scrot /path/to/img    Take a screenshot, if path is left empty the screen-
                                shot function will use $scrot_dir and $scrot_name.
    -su, --upload /path/to/img  Same as --scrot but uploads the scrot to a website.
    --image_host imgur/teknik   Website to upload scrots to.
    --scrot_cmd cmd             Screenshot program to launch

OTHER:
    --config /path/to/config    Specify a path to a custom config file
    --config none               Launch the script without a config file
    --stdout                    Turn off all colors and disables any ASCII/image backend.
    --help                      Print this text and exit
    --version                   Show neofetch version
    -v                          Display error messages.
    -vv                         Display a verbose log for error reporting.

DEVELOPER:
    --gen-man                   Generate a manpage for Neofetch in your PWD. (Requires GNU help2man)


Report bugs to https://github.com/dylanaraps/neofetch/issues
```
