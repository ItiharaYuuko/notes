# Configure the SSH server authorize without password

## When Windows be server

1. Run `ssh-keygen` at Linux or other terminal.
2. On Linux copy `~/.ssh/id_rsa.pub` file to servers `C:\Users\{user}\.ssh\authorized_keys`.
3. On Windows copy `C:\Users\{user}\.ssh\id_rsa.pub` file to `C:\Users\{user}\.ssh\authorized_keys`.
4. Announce `Match Group administrators` and `AuthorizedKeysFile __PROGRAMDATA__/ssh/administrators_authorized_keys` in `C:\ProgramData\ssh\sshd_config`.
5. And on Server run `netsh advfirewall firewall add rule name=sshd dir=in action=allow protocol=TCP localport=22` in terminal, to setup firewall rule for ssh able to through friewall, make connection successful.
6. Run `sc config sshd start=auto` on Server terminal makesure this service running automatic.
7. Run `net stop sshd` and `net start sshd` reboot ssh service for Server.

## When Linux be server

1. Run `ssh-keygen` at Windows or other terminal.
2. Like upon step 2 and 3 only the path be different, on Linux at `~/.ssh/authorized_keys`
3. Run `sshd -P {Port number}` on Server terminal.

* Enjoy