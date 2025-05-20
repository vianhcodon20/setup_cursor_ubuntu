# Install Cursor AI editor on Ubuntu 24.04 

1. Use the Download button on www.cursor.com web site. It will download the `NAME.AppImage` file.

2. Copy the .AppImage file to your Applications directory

```bash
cd ~/Downloads
mkdir -p ~/Applications
mv NAME.AppImage ~/Applications/cursor.AppImage
```

3. Install libfuse2

```bash
sudo apt update
sudo apt install libfuse2
```

4. Make it an executable

```bash
chmod +x ~/Applications/cursor.AppImage
```

5. Run  

```bash
~/Applications/cursor.AppImage --no-sandbox
```

6. Add `cursor` shortcut

Add to `.bashrc` or `.zshrc`

```bash
alias cursor='~/Applications/cursor.AppImage --no-sandbox'


7. Create shortcut on App Desktop

```bash
nano ~/.local/share/applications/cursor.desktop
```

paste

```bash
[Desktop Entry]
Name=Cursor
Comment=AI Code Editor
Exec=/home/ubuntu/Applications/cursor.AppImage --no-sandbox
Icon=utilities-terminal
Terminal=false
Type=Application
Categories=Development;

```
Acept run application

```bash
chmod +x /home/ubuntu/Applications/cursor.AppImage
```

Update database application

```bash
update-desktop-database ~/.local/share/applications
```























