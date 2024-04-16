## grub启动参数增加sched_steal_node_limit=8
> 保存后重启生效
```shell
vi /etc/grub2-efi.cfg

# 在118行末尾添加sched_steal_node_limit=8
    115         else
    116           search --no-floppy --fs-uuid --set=root 1fa16149-f370-422d-ae08-bb749d497255
    117         fi
    118         linux   /vmlinuz-0-rescue-e23302caf5c84b8187ccb44b8ae0481a root=/dev/mapper/bclinux-root ro rd.lvm.lv=bclinux/root rd.lvm.lv=bclinux/swap se        linux=0 console=ttyS0,115200n8 crashkernel=1024M,high smmu.bypassdev=0x1000:0x17 smmu.bypassdev=0x1000:0x15 video=efifb:off video=VGA-1:640x480-32@6        0me sched_steal_node_limit=8
    119         initrd  /initramfs-0-rescue-e23302caf5c84b8187ccb44b8ae0481a.img
    120 }
    121 
    122 ### END /etc/grub.d/10_linux ###
```

## 设置STEAL模式
echo STEAL > /sys/kernel/debug/sched_features
