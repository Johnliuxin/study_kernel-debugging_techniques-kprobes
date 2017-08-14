# Note
This example is copied from kernel original source code : samples/kprobes/jprobe_example.c

# Pre-conditions
First of all, you need to enable kernel to support kprobe.  

When build your kernel, you must enable CONFIG_KPROBES.   
it is better to enable CONFIG_KALLSYMS and CONFIG_KALLSYMS_ALL at the same time.

# Build
` cd debugging_techniques/kprobes/jprobe `  
` export CROSS_COMPILE, ARCH, KERNELDIR `  
` make `

# Usage
` dmesg -c `  
` insmod jprobe_exam.ko `  
` any shell cmd `  
` dmesg `

# Result
> [ 2654.651724] j_do_fork: clone_flags = 0x1200011, stack_start = 0x0 stack_size = 0x0  
> [ 2658.088043] j_do_fork: clone_flags = 0x1200011, stack_start = 0x0 stack_size = 0x0