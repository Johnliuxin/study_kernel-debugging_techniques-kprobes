# Note
This example is copied from kernel original source code : samples/kprobes/kprobe_example.c

# Pre-conditions
First of all, you need to enable kernel to support kprobe.  

When build your kernel, you must enable CONFIG_KPROBES.   
it is better to enable CONFIG_KALLSYMS and CONFIG_KALLSYMS_ALL at the same time.

# Build
` cd debugging_techniques/kprobes/kprobe `  
` export CROSS_COMPILE, ARCH, KERNELDIR `  
` make `

# Usage
` dmesg -c `  
` insmod kprobe_exam.ko `  
` any shell cmd `  
` dmesg `

# Result
> [ 3916.267424] pre_handler: p->addr = 0xc0030c38, ip = 50c5387d, flags = 0x40000033  
> [ 3916.267431] post_handler: p->addr = 0xc0030c38, flags = 0x40000033  
> [ 3918.527629] pre_handler: p->addr = 0xc0030c38, ip = 50c5387d, flags = 0x40050033  
> [ 3918.527635] post_handler: p->addr = 0xc0030c38, flags = 0x40050033  