# bpftrace-syscall
What kernel is doing then i run a program


for run^
sudo bpftrace trace.bt  -I /usr/lib/modules/$(uname -r)/build/include/uapi/linux  -I /usr/lib/modules/$(uname -r)/build/include/linux $1 2>&1 | tee /tmp/out
