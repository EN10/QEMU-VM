# QEMU VM

Running Debian on Windows without Admin rights

Download QEMU
-
* [Download](https://qemu.weilnetz.de/w64/)
* Extract
* [List of files](https://github.com/EN10/QEMU-VM/blob/master/filelist.txt) need to run linux on windows.    

Slax Debian iso
-
[Slax](https://www.slax.org/#purchase)

Run
-
    .\qemu-system-x86_64.exe -cdrom .\slax-64bit-9.8.0.iso  -m 2048
 
 Snapshots
-
    .\qemu-img.exe create -f qcow2 slax.img 400M
    .\qemu-system-x86_64.exe -cdrom .\slax-64bit-9.8.0.iso -hda .\slax.img -m 2048
    
Open Monitor:	Ctrl+Alt+2
    
    savevm name
    loadvm name

Hardware Acceleration

*    [Download](https://github.com/intel/haxm/releases)

    .\qemu-system-x86_64.exe -cdrom .\slax-64bit-9.8.0.iso -hda .\slax.img -m 2048 -accel hax

Ref:      [HAXM](https://www.qemu.org/2017/11/22/haxm-usage-windows)  
