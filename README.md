# linux-newbie-101
Linux / \*nix getting started

```bash
docker run --rm -it --name linux ubuntu
```

- which system you are usung? 
  ```bash
  uname
  uname -v
  uname -r
  uname -a
  ```
- re-run previous command with sudo
  ```bash
  sudo !!
  ```
  or just press `CTRL+U`, type sudo and press `CTRL+Y` (read next why)
- cut text to the end of a line: `CTRL+K` and next after to revert text back: `CTRL+Y`
- cut text to the beginning of a line: `CTRL+U` and next after to revert text back: `CTRL+Y`
- cut words delimited by spaces backwords: `CTRL+W` and next after to revert text back: `CTRL+Y`
- how check which files / directories in a directory?
  ```bash
  ls
  ls path/to/dir
  ls -lah /
  ```
- many ways to tailg...
  ```bash
  tail file.log
  tail -f file log  # follow
  cat file.log
  less file.log     # pess `SHIFT+F` to go to the end of the file
  less +F file.log  # will load whole file in memory and starts from the end
                    # then press `CTRL+C` to start scroll
                    # and press `CTRL+F` to attach back for tailing
  more file.log
  cat file.log | less
  cat file.log | more
  ```
- how do you can get direcotry size?
  ```bash
  du -sh path/to/dir
  ```
- how much free space do you have?
  ```bash
  df -ah
  ```
- how dou you managing partitions on your system?
  ```bash
  # checking for existing mounts
  mount

  # mount new devise: mount $deviceAddress $mountPoint
  mount /dev/sda /mnt

  ls /mnt
  cat /etc/fstab
  ```
- who you can check if service is running and start it if not?
  ```bash
  # service $serviceName command
  service udev status
  service udev start
  service udev stop
  
  systemctl udev status
  ```
- what's your IP address?
  ```bash
  # ifconfig #interfaceName

  ifconfig
  ifconfig eth0

  ip addr show
  ip addr show eth0
  ```
- how would you check listenning / openning ports?
  ```bash
  netstat
  netstat -a
  netstat -tulpn
  sudo netstat -tulpn
  ```
- how would you check of CPU usage per process?
  ```bash
  # ps waux | grep $process
  ps waux | grep nginx

  top
  htop
  ```
- RTFM
  ```bash
  # man $command

  man ps

  # google / stackoverflow
  ```

links:

- [YouTube: Top 10 linux Job Interview Questions](https://www.youtube.com/watch?v=l0QGLMwR-lY)
