# one-monokai-gnome-terminal-color-theme
One Monokai color theme for GNOME Terminal

### How to apply theme:
Download 'one-monokai.dconf' file
1. Create a new profile in GNOME Terminal settings, rename it to e.g. 'default'. The name will be overwritten on import, you can then rename it again to what you want
   This step is not necessary if you already have created a profile that is not the default "unnamed" profile.
2. Set the new profile as the default profile
3. run `dconf dump /org/gnome/terminal/legacy/profiles:/`, see that it returns output similar to this:

    $ dconf dump /org/gnome/terminal/legacy/profiles:/
    [/]
    list=['e27d087d-18c4-4b72-83be-c84103543515']
    default='e27d087d-18c4-4b72-83be-c84103543515'

    [:e27d087d-18c4-4b72-83be-c84103543515]
    visible-name='default'

4. Copy the UUID of the created profile (in the example it is :e27d087d-18c4-4b72-83be-c84103543515 )
5. Run `dconf load /org/gnome/terminal/legacy/profiles:/:e27d087d-18c4-4b72-83be-c84103543515/ < one-monokai.dconf`
   This will import the settings from the file to the profile and also apply it as the current profile.
6. Modify other settings as needed.

### Credits:
- Colors picked from https://github.com/azemoh/vscode-one-monokai/blob/master/themes/OneMonokai-color-theme.json
- Instructions adapted from http://davidzchen.com/tech/2020/07/21/importing-and-exporting-gnome-terminal-color-schemes.html
