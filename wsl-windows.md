# WSL Setup Guide

## 1. Run PowerShell as Administrator

1. Press `Win + X` and select **PowerShell (Admin)**.
2. Confirm the UAC prompt.

## 2. Install WSL

Run the following command:

```powershell
wsl --install
```

For more details, refer to the official documentation:  
[Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

## 3. Download Windows Terminal

For a better experience, install Windows Terminal from the Microsoft Store:

[Windows Terminal Documentation](https://learn.microsoft.com/en-us/windows/terminal/)

## 4. Set Windows Terminal Default Profile to Ubuntu

1. Open **Windows Terminal**.
2. Click the **▼** button next to the new tab button and select **Settings**.
3. Under "Startup", find **Default profile**.
4. Select **Ubuntu** from the dropdown menu.
5. Click **Save**.

## 5. (Optional) Add a Theme to Windows Terminal

You can customize the terminal theme using:

- [Terminal Splash Themes](https://terminalsplash.com/?ref=zimmergren.net&utm_campaign=zimmergren&utm_medium=blog&utm_source=zimmergren)

Or manually add the following **Catppuccin Macchiato** theme:

```json
{
  "name": "Catppuccin Macchiato",
  "black": "#494d64",
  "red": "#ed8796",
  "green": "#a6da95",
  "yellow": "#eed49f",
  "blue": "#8aadf4",
  "purple": "#f5bde6",
  "cyan": "#8bd5ca",
  "white": "#b8c0e0",
  "brightBlack": "#5b6078",
  "brightRed": "#ed8796",
  "brightGreen": "#a6da95",
  "brightYellow": "#eed49f",
  "brightBlue": "#8aadf4",
  "brightPurple": "#f5bde6",
  "brightCyan": "#8bd5ca",
  "brightWhite": "#b8c0e0",
  "background": "#24273a",
  "foreground": "#cad3f5",
  "selectionBackground": "#5b6078",
  "cursorColor": "#f4dbd6"
}
```

To apply, open **Windows Terminal Settings**, select Defaults under Profiles, navigate to **Appearance**, and select the theme under **Color Schemes**.

## 6. (Optional) Install a Nerd Font

For better icon and glyph support, install a Nerd Font like **FiraCode Nerd Font**:

- [Download Nerd Fonts](https://www.nerdfonts.com/#home)

After installation:
1. Open **Windows Terminal Settings**.
2. Select Defaults under Profiles.
3. Under **Appearance**, change the Font face to **FiraCode Nerd Font**.
4. Click **Save**.
