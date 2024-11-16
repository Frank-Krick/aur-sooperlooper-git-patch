# AUR sooperlooper git patch

Patches the build errors in the sooperlooper-git AUR script which happens
because the default error level for the c compiler in Arch Linux is
`-fpermissive`.

To apply the patch and install sooperlooper do the following:

1) Install git, if not done already
1) Checkout the repository for sooperlooper-git

```bash
git clone https://aur.archlinux.org/sooperlooper-git.git
```

1) Navigate into the repository

```bash
cd sooperlooper-git/
```

1) Download the patch

```bash
wget https://raw.githubusercontent.com/Frank-Krick/aur-sooperlooper-git-patch/main/patchfile
```

1) Apply the patch

```bash
git apply patchfile
```

1) Build the package, use `-s` to automatically install dependencies

```bash
makepkg -s
```

1) Install the package

```bash
pacman -U <package>
```

For me `<package>` is `sooperlooper-git-r557.c5e22ce-1-x86_64.pkg.tar.zst`,
so I would call `pacman -U sooperlooper-git-r557.c5e22ce-1-x86_64.pkg.tar.zst`.

Your package name might differ depending on version and architecture for example.
