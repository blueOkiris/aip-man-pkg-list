# The Global Package List for the Aip-Man

## Description

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

Optionally, if the AppImage comes as a `.tar.gz` or `.zip` instead of just a .AppImage, you can add `"compressed": true`, and if the AppImage has versions for different architectures, you can add the `alt_arch_urls` entry, which is formatted like so:

```
"alt_arch_urls": {
    "<arch>": "<url>",
    ...
    "<arch>": "<url>"
}
```

Note:

- The default url should be x86_64
- The list of architecture names is that of Rust `std::env::consts::ARCH`. Here's Rust's [documentation on that](https://doc.rust-lang.org/std/env/consts/constant.ARCH.html).

Make a commit like "Add \<whatever application\>" or "Update for \<application\> to \<version\>," post a PR, and I'll look at it and merge it in.

Thanks!

## Maintaining

I, blueOkiris, will keep the download links and versions up to date from their mainstream monthly (1st weekend of each month) or when I happen to notice a new version and can get to it. I use aip-man myself, so I want my packages up to date.

However, I'm one person, so if you see a chance to update, create a PR. I'd love your help.
