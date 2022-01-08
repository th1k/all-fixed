## How To Clone Fixed VDI To Dynamic VDI On VirtualBox

While there is no way to actually switch a VDI between fixed-size and dynamic, you can clone the existing VDI into a new one with different settings with VBoxManage.

    VBoxManage clonehd [old-VDI] [new-VDI] --variant Standard
    VBoxManage clonehd [old-VDI] [new-VDI] --variant Fixed

If you want to expand the capacity of a VDI, you can do so with

    VBoxManage modifyhd [VDI] --resize [megabytes] 

Ex. VBoxManage modifyhd Ubuntu12.vdi --resize 30000 (30GB)

http://kamaths.org/virtualbox-increase-hard-disk-size-of-linux-guest/

On a linux guest you need to resize the partion to take advantage of the resized disk.


**Examples:**

    VBoxManage clonehd Ubuntu12.vdi Ubuntu12Dynamic.vdi --variant Standard
    
**Source:**
- http://brainwreckedtech.wordpress.com/2012/01/08/howto-convert-vdis-between-fixed-sized-and-dynamic-in-virtualbox/
- http://www.webdesignblog.asia/software/linux-software/resize-virtualbox-disk-image-manipulate-vdi/#comment-474
- https://gist.github.com/stormwild/6403128
