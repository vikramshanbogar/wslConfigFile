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
