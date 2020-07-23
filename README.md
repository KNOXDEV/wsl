# wsl

A [scoop bucket](https://scoop.sh/) of installers for [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about).

Make absolutely certain to [enable the WSL feature](https://docs.microsoft.com/en-us/windows/wsl/install-win10) first, like so:
```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Install scoop like this:
```powershell
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

Then install this software bucket like this:
```powershell
scoop bucket add wsl https://git.irs.sh/KNOXDEV/wsl
```

Now you can quickly and automatically install the software registered here. No Windows Store necessary.
For example, to install Ubuntu 20.04 LTS, just use:
```powershell
scoop install wsl-ubuntu2004
```
For a full list of current supported distros, check the bucket, or just run:
```powershell
scoop search wsl-
```

That's it! The software in this bucket should not be considered stable and may not install successfully while its a Work In Progress.

### notes

* I decided to not add hashes to the manifest due to a lack of consistent versioning information. It's unclear if Microsoft will push in-place upgrades of the distro download links I'm using, but that is what I suspect, in which case the hashes do more harm than good. The installers themselves have built-in integrity checks, so I'm not too concerned about it.

* Whichever distro you install *first* will be your default from then on out. Your default distro is the one that opens when you `Right Click > Open Linux shell here` or use `wsl.exe` from the command line. You can reset your default by using [wslconfig](https://docs.microsoft.com/en-us/windows/wsl/wsl-config#managing-multiple-linux-distributions).

* Uninstalling a distro and reinstalling it with scoop will **DELETE** everything stored in that distros filesystem and set it back to scratch. This includes if you UPDATE the distro via scoop, although I have no plans to publish updates to existing distro manifests since you can just update them with a package manager.

* Yes, this works on Windows 10 LTSC :)

* ~~Yes, there are distros I haven't added yet. Feel free to add them or make changes.~~ I actually don't know of any distros I'm missing anymore. Create a pull request or issue to suggest an addition to the repo.
