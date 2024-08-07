# bpftrace-syscall
What kernel is doing then i run a program


for run^
```
sudo bpftrace trace.bt  -I /usr/lib/modules/$(uname -r)/build/include/uapi/linux  -I /usr/lib/modules/$(uname -r)/build/include/linux $1 2>&1 | tee /tmp/out
```

show result:
```
sudo bpftrace /home/odity/bin/bpftrace_process.bt -I /usr/lib/modules/$(uname -r)/build/include/uapi/linux  -I /usr/lib/modules/$(uname -r)/build/include/linux ssh 2>&1 | tee /tmp/out
Attaching 315 probes...
1357770484 µs:   11214  ssh                   tracepoint:syscalls:sys_enter_brk [1] arg0:0 
1357770502 µs:   11214  ssh                   tracepoint:syscalls:sys_enter_brk [1] arg0:1092281184 
1357770618 µs:   11214  ssh                tracepoint:syscalls:sys_enter_access [2] arg0:0x71adb70cc3a0 arg1:4 
1357770621 µs:   11214  ssh                tracepoint:syscalls:sys_enter_access [2] arg0:0xffff9b7a411ab6a8 arg1:1416866560 
1357770641 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:-100 arg1:0x71adb70cc3a0 arg2:524288 arg3:0 
1357770643 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:796755192 arg1:0x14f31a35473ab00 arg2:796755192 arg3:15312 
1357770672 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:3 arg1:0x7ffc94141f70 
1357770676 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:1092285000 arg1:0x14f31a35473ab00 
1357770687 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:3 
1357770689 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:1092265920 
1357770708 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:-100 arg1:0x71adb70cb11d arg2:524288 arg3:0 
1357770710 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:796755192 arg1:0x14f31a35473ab00 arg2:796755192 arg3:15664 
1357770722 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:3 arg1:0x7ffc94141490 
1357770723 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:1092285000 arg1:0x14f31a35473ab00 
1357770728 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:(nil) arg1:285519 arg2:1 arg3:2 arg4:3 
1357770730 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958480 arg4:1463959368 
1357770762 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:3 
1357770764 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:1092265920 
1357770838 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:-100 arg1:0x71adb70d6f80 arg2:524288 arg3:0 
1357770840 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:796755192 arg1:0x14f31a35473ab00 arg2:796755192 arg3:15728 
1357770860 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_read [3] arg0:3 arg1:0x7ffc94141608 arg2:832 
1357770863 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_read [3] arg0:1092273552 arg1:0x14f31a35473ab00 arg2:1092273552 
1357770873 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:3 arg1:0x7ffc94141490 
1357770875 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:1092285000 arg1:0x14f31a35473ab00 
1357770885 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:(nil) arg1:8192 arg2:3 arg3:34 arg4:-1 
1357770887 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958736 arg4:1463959368 
1357770922 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:(nil) arg1:338736 arg2:1 arg3:2050 arg4:3 
1357770924 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958552 arg4:1463959368 
1357770938 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb7007000 arg1:249856 arg2:5 arg3:2066 arg4:3 
1357770939 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958800 arg4:1463959368 
1357770975 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb7044000 arg1:40960 arg2:1 arg3:2066 arg4:3 
1357770976 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958608 arg4:1463959368 
1357770994 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb704e000 arg1:12288 arg2:3 arg3:2066 arg4:3 
1357770996 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958560 arg4:1463959368 
1357771052 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:3 
1357771053 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:1092265920 
1357771075 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:-100 arg1:0x71adb7051510 arg2:524288 arg3:0 
1357771077 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:796755192 arg1:0x14f31a35473ab00 arg2:796755192 arg3:15896 
1357771093 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_read [3] arg0:3 arg1:0x7ffc941415e8 arg2:832 
1357771095 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_read [3] arg0:1092273552 arg1:0x14f31a35473ab00 arg2:1092273552 
1357771102 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:3 arg1:0x7ffc94141470 
1357771104 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:1092285000 arg1:0x14f31a35473ab00 
1357771111 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:(nil) arg1:5037280 arg2:1 arg3:2050 arg4:3 
1357771112 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958880 arg4:1463959368 
1357771131 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6a4c000 arg1:3485696 arg2:5 arg3:2066 arg4:3 
1357771133 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958368 arg4:1463959368 
1357771180 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6d9f000 arg1:823296 arg2:1 arg3:2066 arg4:3 
1357771182 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958152 arg4:1463959368 
1357771203 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6e68000 arg1:405504 arg2:3 arg3:2066 arg4:3 
1357771205 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958360 arg4:1463959368 
1357771245 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6ecb000 arg1:11488 arg2:3 arg3:50 arg4:-1 
1357771247 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958440 arg4:1463959368 
1357771304 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:3 
1357771306 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:1092265920 
1357771328 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:-100 arg1:0x71adb7051a40 arg2:524288 arg3:0 
1357771330 µs:   11214  ssh                tracepoint:syscalls:sys_enter_openat [4] arg0:796755192 arg1:0x14f31a35473ab00 arg2:796755192 arg3:15320 
1357771350 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_read [3] arg0:3 arg1:0x7ffc941415c8 arg2:832 
1357771351 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_read [3] arg0:1092273552 arg1:0x14f31a35473ab00 arg2:1092273552 
1357771359 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:3 arg1:0x7ffc94141450 
1357771360 µs:   11214  ssh              tracepoint:syscalls:sys_enter_newfstat [2] arg0:1092285000 arg1:0x14f31a35473ab00 
1357771367 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:(nil) arg1:98320 arg2:1 arg3:2050 arg4:3 
1357771369 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463959032 arg4:1463959368 
1357771390 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6fe8000 arg1:57344 arg2:5 arg3:2066 arg4:3 
1357771391 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958280 arg4:1463959368 
1357771495 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6ff6000 arg1:24576 arg2:1 arg3:2066 arg4:3 
1357771497 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958536 arg4:1463959368 
1357771524 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0x71adb6ffc000 arg1:8192 arg2:3 arg3:2066 arg4:3 
1357771526 µs:   11214  ssh                  tracepoint:syscalls:sys_enter_mmap [5] arg0:0xffff9b7a411ab1b0 arg1:1416866560 arg2:1092268464 arg3:1463958184 arg4:1463959368 
1357771610 µs:   11214  ssh                 tracepoint:syscalls:sys_enter_close [1] arg0:3 
```
