# colemak-dh-jp
Adds Colemak-DH variant to Japanese keyboard in X11

## How to install
Open the `jp` keyboard layout file for X11 in a text editor with root priveledges
```sh
sudo nano /usr/share/X11/xkb/symbols/jp
```

Add these at the end of the file
```c-like
partial alphanumeric_keys
xkb_symbols "colemak-dh" {

    include "jp(OADG109A)"

    name[Group1]= "Japanese (Colemak-DH)";

    key <AD03>	{[ f, F			]};
    key <AD04>	{[ p, P			]};
    key <AD05>	{[ b, B			]};
    key <AD06>	{[ j, J			]};
    key <AD07>	{[ l, L			]};
    key <AD08>	{[ u, U			]};
    key <AD09>	{[ y, Y			]};
    key <AD10>	{[ semicolon, plus	]};

    key <AC02>	{[ r, R			]};
    key <AC03>	{[ s, S			]};
    key <AC04>	{[ t, T			]};
    key <AC06>	{[ m, M			]};
    key <AC07>	{[ n, N			]};
    key <AC08>	{[ e, E			]};
    key <AC09>	{[ i, I			]};
    key <AC10>	{[ o, O			]};

    key <AB01>	{[ x, X			]};
    key <AB02>	{[ c, C			]};
    key <AB03>	{[ d, D			]};
    key <AB05>	{[ z, Z			]};
    key <AB06>	{[ k, K			]};
    key <AB07>	{[ h, H			]};
};
```

Save the file, close nano, and then run
```sh
setxkbmap jp -variant colemak-dh
```
to apply the new keyboard layout
