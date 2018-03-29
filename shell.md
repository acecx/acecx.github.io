## 常用shell命令
#### vagrant homestead 时间与本机同步
```
VBoxManage guestproperty set homestead-7 "/VirtualBox/GuestAdd/VBoxService/--timesync-set-threshold" 10000
```
- ##### get status of time sync
```
VBoxManage getextradata <vm-name> VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled 
```
- ##### disable time sync
```
VBoxManage setextradata <vm-name> VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled 1
```
- ##### enable time sync
```shell
VBoxManage setextradata <vm-name> VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled 0
```