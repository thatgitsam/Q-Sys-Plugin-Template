# Q-Sys-Plugin-Template

Development Template & Guide for Q-Sys LUA Plugins on Q-Sys Community, for deployment to GitHub Package Registry

## Development

Clone a plugin repository to your development folder (Note: Not your User Plugins folder)

```ps2
git clone
```

Navigate to your User Plugins folder

```ps2
%userprofile%\Documents\QSC\Q-Sys Designer\Plugins
```

To develop plugins, copy the .qplug to your plugins folder and copy back when done.

### Symbolic links

You may use a symantic link, designer does not reload them when saved so needs to be restarted to pick up on changes, possibly due to how it watches files.

Create a symbolic link to the .qplug file in the cloned repository using PowerShell

```ps2
New-Item -ItemType SymbolicLink -Path ".\q-sys-plugin-template.qplug" -Target "C:\yourpath\GitHub\Q-Sys-Plugin-Template\content\q-sys-plugin-template.qplug"
```

## Deployment

### Packing

Download the latest version of nuget if not present

```
https://dist.nuget.org/win-x86-commandline/latest/nuget.exe
```
