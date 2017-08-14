# Note
This example is copied from kernel original source code : samples/kprobes/kretprobe_example.c

# Pre-conditions
First of all, you need to enable kernel to support kprobe.  

When build your kernel, you must enable CONFIG_KPROBES.   
it is better to enable CONFIG_KALLSYMS and CONFIG_KALLSYMS_ALL at the same time.

# Build
` cd debugging_techniques/kprobes/kretprobe `  
` export CROSS_COMPILE, ARCH, KERNELDIR `  
` make `

# Usage
` dmesg -c `  
` insmod kretprobe_exam.ko `  
` any shell cmd `  
` dmesg `

# Result
> [ 5001.823611] _do_fork returned 757 and took 673974 ns to execute  
> [ 5005.727753] _do_fork returned 758 and took 675974 ns to execute  