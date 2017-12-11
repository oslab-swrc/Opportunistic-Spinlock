# oticke+, qspinlock+
oticket+ and qspinlock+ is the enhanced version of paravirtualized ticket lock and queue spinlock 

# What is oticket+, qspinlock+?

qspinlock+ is the improved KVM-side part of the existing paravirt qspinlock. Instead of HALT EXIT in pvqspinlock, pvqspinlock+ uses hypercall to minimize a delay and boosts vcpus which is presumed to be a lock holder minimizing lock holder preemption problem. oticket+ is based on ticket spinlock which is used before qspinlock.  

oticket+ ( kernel 4.5.0-rc2 )
qspinlock+ ( kernel 4.9.26 )

# How to Use

After patching and building kernel, reboot and install kvm and kvm-intel module.
(oticket+ patch: kernel 4.5.0-rc2, qspinlock+ patch: kernel 4.9.26)

# LICENSE

It is distributed under the GNU General Public License - see the
  accompanying COPYING file for more details. 


You can find more detail in here(https://www.actapress.com/Abstract.aspx?paperId=456169).

