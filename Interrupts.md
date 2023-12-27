1. [LINK 1] https://linux-kernel-labs.github.io/refs/heads/master/lectures/interrupts.html
2. [LINK 2] https://www.scs.stanford.edu/05au-cs240c/lab/i386/s09_01.htm#:~:text=If%20detected%20during%20the%20instruction,the%20instruction%20to%20be%20restarted.&text=A%20trap%20is%20an%20exception,which%20the%20exception%20was%20detected.

__TRAPS__

An abort is an exception that permits neither precise location of the instruction causing
the exception nor restart of the program that caused the exception. Aborts are used to
report severe errors, such as hardware errors and inconsistent or illegal values
in system tables. 

1. _Exception without Precise Location:_

An "abort" in the context of exception handling refers to a situation where the program
encounters a severe error, but the system cannot precisely identify the location in the
code where the error occurred. Unlike some other exceptions that provide detailed
information about the point of failure, an abort lacks this precision.

2. _No Program Restart:_

When an abort occurs, it signifies that the error is so severe that the program cannot
safely continue its execution. Unlike certain types of exceptions that might be caught
and handled, an abort typically results in the termination of the program, and there
is no attempt to restart or recover from the error condition.

3. _Usage for Severe Errors:_

Aborts are specifically designed to handle severe errors, including those associated 
with hardware failures or situations where the integrity of critical system data is
compromised. Examples include inconsistencies or illegal values in essential system
tables, which are data structures used by the operating system to manage various
aspects of system behavior.

To elaborate further:

4. _Hardware Errors:_

Aborts are often used to handle errors at the hardware level, such as faults in the
CPU or memory. These errors may indicate a serious problem that prevents the program
from continuing safely. 

4.1. _Inconsistent or Illegal Values in System Tables:_

System tables contain crucial information about the state of the system. If the values
in these tables become inconsistent or if illegal values are detected, it may lead to
unpredictable behavior. Aborting the program in such cases is a way to prevent further 
execution that could exacerbate the problem. 

In practical terms, the concept of "abort" is
often associated with functions like abort() in the C Standard Library, which explicitly
triggers abnormal termination, and the SIGABRT signal in Unix-like systems. When a program
encounters a condition that warrants an abort, it is a way for the system to halt execution,
report the severe error, and prevent potential damage or instability.







