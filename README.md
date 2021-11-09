# oticket+, qspinlock+
oticket+ and qspinlock+ is the enhanced version of paravirtualized ticket lock and queue spinlock 

qspinlock+ is the improved KVM-side part of the existing paravirt qspinlock. Instead of HALT EXIT in pvqspinlock, pvqspinlock+ uses hypercall to minimize a delay and boosts vcpus which is presumed to be a lock holder minimizing lock holder preemption problem. oticket+ is based on ticket spinlock which is used before qspinlock.  

The repository is provided under the terms of the GNU General Publuc License v2.0.

# How to Use

After patching and building kernel, reboot and install kvm and kvm-intel module.
```
- oticket+ was developed on Linux 4.5.0-rc2
- The Linux kernel source is available in ./linux-4.5-rc2/
- Build and install the kernel.
```
```
- qspinlock+ was developed on Linux 4.9.26
- The Linux kernel source is available in ./linux-4.9-26
- Build and install the kernel.
```
