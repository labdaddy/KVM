##### If the GUI is missing in the CentOS distro
- In case you installed a VM intending to have a GUI and somehow it installed without (like the minimal version even though using the full DVD version), you can always add the gnome desktop after the fact.
- Let’s install GNOME Desktop with the following command: `yum groups install "GNOME Desktop"`
- It will take a while to install the packages needed for GNOME. Like 15 minutes so be patient.
- Once done use `startx` command.
- You need to go through accepting a license, creating a user, configuring language, keyboard type to set up for the first time, and finally, you will have the CentOS desktop.
- We are not done yet. When you reboot your CentOS, you will see the command prompt again. So you need to preserve the settings to start in graphical mode every time you boot the OS. Open a terminal and execute the following command: `systemctl set-default graphical.target`
- Restart CentOS, and it should be booted in GNOME GUI mode.
- If you are not a GNOME fan then Alternatively, you may install the KDE environment with this command: `yum  groups install `KDE Plasma Workspaces`
