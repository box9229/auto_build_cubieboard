auto_build_cubieboard
=====================

Automatic build uboot, linux-kernel from source code for Cubieboards. Include for CB1,CB2,CB3,CB4

## Prepare
 
Before you start, Some packets must be installed in you environment.

    # apt-get install uboot-mkimage kpartx dosfstools dos2unix device-tree-compiler
    
And you also need ARM cross-compiler such as "arm-linux-gnueabihf-xxx" and "arm-linux-gnueabi-xxx"

## How to use

    # sudo ./auto_build.sh cb1|cb2|cb3|cb4


***

## Note

(1) If you want to build linux kernel for CB4. It only work with ARM cross-compiler(ARMEL) version 4.6.x.
Because the CB4 kernel source need two compiler option: ‘--min_array_alignment=4’ '--no_unaligned_access'. 
Only ARM cross-compiler(ARMEL) 4.6.x support these two options.


從source code 開始打造最基本的Debian linux system

這幾天將以前寫好的一些自動compile uboot 及 linux kernel 的script 給放到GitHub 去了.
這些script 是提供給一些對於source code 有偏執狂, 以及有興趣研究Cubieboard linux system 如何製作出來的人, 大家可以來研究及討論.

我利用這些script 從source code 開始, 建立出uboot 及linux kernel 的binary, 再配合動手打造Debian root filesystem for ARM這篇文章, 就可以打造出可以執行的Debian image file 了, 將此image file 燒到TF card 中, 放到Cubieboard1, Cubieboard2或 Cubietruck 板子就可以跑起來了.

詳細的流程等以後有空再來描述. 有興趣的人請到GitHub參考source code.

[2014/12/17 更新] 目前已經可以支援Cubieboard 4 (CC-A80) 板子了.
