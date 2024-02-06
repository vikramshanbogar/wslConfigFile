https://vikramshanbogar.medium.com/wsl-config-file-4cc5508e43e6

if you are concerned that wsl is using more Resources then its supposed to, wsl config file is the solution provided by microsoft.

create a `.wslconfig in %USERPROFILE%`

Below are the configurations I have setup for my WSL instance(ubuntu) maybe edit/add options for CPU cores and RAM assignment

```
[wsl2]
memory=4GB
processors=2
swap=1GB

```

- `memory` is the maximum amount your ram that WSL will use;
- `processors` is the alocated cores to your WSL vm;
- `swap` is the size of the swap file;
- `swapFile` is the location of your swap and to my knowledge is used by all WSL vm's; notice the double slashes in the path, they are mandatory for the path.

Start your WSL VM as you normally would.

**Set the systemd flag set in your WSL distro settings**
You will need to edit the wsl.conf file to ensure systemd starts up on boot.

Add these lines to the /etc/wsl.conf (note you will need to run your editor with sudo privileges, e.g: sudo nano /etc/wsl.conf):
```
[boot]
systemd=true
```
And close out of the nano editor using CTRL+O to save and CTRL+X to exit.
