# Printer macros

This repo provides use klipper printer macros

## Important features

* Useful klipper macros

## How to install

The instructions assume that you have a up to data and working moonraker installation. If not start with updating your moonraker first. There are two methods that can be used to install these configs as listed below.

### Add updater section

Open your moonraker.conf and add

```ini
[update_manager printer-macros]
type: git_repo
channel: dev
primary_branch: main
path: ~/printer-macros
origin: https://github.com/geoff-coppertop/printer-macros.git
managed_services: klipper
```

below the mainsail updater section.

### Manual clone

SSH into your PI and run the following,

```bash
cd ~/printer_data/config/
git clone https://github.com/geoff-coppertop/printer-macros.git
```

Then open your moonraker.conf and add

```ini
[include ~/printer_data/config/printer-macros/moonraker.conf]
```

below the mainsail updater section.

### How to setup

The setup process is completed by simply adding the following,

```ini
[include macro.cfg]
```

to your printer.cfg file. Be aware the file will show up as read only. This was intended by use.
