
### Favorite Softwares

- **Haruna** media player: Haruna
- **zeal** : help Documents GUI
- **gwenview**: Image Cropper
- Open3D engine : https://o3debinaries.org/download/linux.html
- https://developer.hashicorp.com/terraform/install?product_intent=terraform
- https://learn.microsoft.com/en-in/dotnet/core/install/linux-debian
- https://learn.microsoft.com/en-us/powershell/scripting/install/install-debian
- 

##### Enable Remote Desktop on ubuntu
this configuration will enable remote access of the machine from the remote clients like 'remmina' on Linux and 'remote desktop' on window
```
sudo apt install xrdp
sudo systemctl enable --now xrdp

#optional
sudo ufw allow from any to any port 3389 proto tcp
```

##### LoadingNTFSonParrotOS
#ParrotOS


**find the UUID of all the partitions, so that it can be updated in fstab**
```
$sudo blkid
```
**create folder with name ntfs inside the /mnt where partition is to be loaded.**
```
$sudo mkdir -p /mnt/ntfs
```
**append line as sample below**
```
$sudo nano /etc/fstab
UUID=af406bcd-cddb-4095-8456-fdf8dfe37665 /mnt/ntfs ntfs defaults 0 0
```
load the changes 
$sudo systemctl daemon-reload
#This command will reload the fstab config and so change will be applied without restart.



##### install Oracle JDK 

```
sudo apt-add-repository ppa:webupd8team/java  
sudo apt-get update 
sudo apt-get install oracle-java8-installer 
```



##### Ubuntu-- Cybersecurity Tools installations

**Source : Apt**

| Tool     | Command |
| -------- | ------- |
| nmap     |         |
| ettercap |         |
|          |         |

**Source : GitHub**

| Tool         | URL                                      |
| ------------ | ---------------------------------------- |
| theHarvester | https://github.com/laramies/theHarvester |
|              |                                          |

