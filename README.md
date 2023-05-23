# JetBackup5-to-cPanel

[JetBackup 5](https://www.jetbackup.com/) introduces multi-panel support, meaning that backups created in a cPanel server, for example, can be restored on a DirectAdmin server (and vice versa).
To achieve that, the JetBackup team has to create its own unique backup structure (unlike JetBackup 4 which was based on the native cPanel backup structure).

Here is a “Quick & Dirty” bash magic script that will convert a JetBackup 5 structure into cPanel backup structure ("cpmove" file). The generated cpmove file can be restored on any cPanel server (using `/scripts/restorepkg`) regardless of JetBackup (doesn’t have to be installed on the server).

The script can generate a cPanel backup from an already downloaded backup file (usually located at `/usr/local/jetapps/usr/jetbackup5/downloads`), or you can provide a username, and it will fetch the latest backup automatically (given that there are full active backups for that account).

## Quick use

```bash
wget https://raw.githubusercontent.com/wnpower/JetBackup5-to-cPanel/master/jb5_to_cpanel_convertor.sh && bash jb5_to_cpanel_convertor.sh
```

## Preview

<p align="center">
  <img src="https://user-images.githubusercontent.com/32086536/240131231-ece7e09b-6051-476a-8a4d-805557373008.png" width="200">
  <img src="https://user-images.githubusercontent.com/32086536/240131272-000c5632-92c4-44b7-a7dd-88be1d93f417.png" width="200">
</p>

## Disclaimer

Replicated from [The Lazy Admin Blog](https://thelazyadmin.blog/convert-jetbackup-to-cpanel), october 06, 2022 version. Please visit the original author for more updates.
Use at your own risk.