# The Global Package List for the Aip-Man

The [AppImage Package Manager](https://github.com/blueOkiris/aip-man) pulls the pkgs.json file from this repo, parses it, and uses it to install and upgrade packages.

If you'd like to add a package, you're simple one commit and PR away!

Format package listings as so:

```
[
    ...
    {
        "name": "<package name>",
        "version": "<version string>",
        "description": "<description>",
        "url": "<link to file to download>"
    }, {
        "name": "audacity",
        "version": "3.2.3",
        "description": "Audacity is an easy-to-use, multi-track audio editor and recorder for Windows, macOS, GNU/Linux and other operating systems. Audacity is free, open source software.",
        "url": "https://github.com/audacity/audacity/releases/download/Audacity-3.2.3/audacity-linux-3.2.3-x64.AppImage"
    },
    ...
]
```
Make a commit like "Add \<whatever application\>" or "Update for \<application\> to \<version\>," post a PR, and I'll look at it an merge it in.

Thanks!
