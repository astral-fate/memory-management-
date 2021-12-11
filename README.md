# memory-management-

previously, we said that the os is responsible to manage thr hardware components. 
one if these components is how much the process (program under execution) can use the actual 
physical memory. 

the os manages the memory by allocating a virtual adress space for every procces, and that adress includes the details and thr heap, stack and data of this process.
then the os, with thr help of the memory management unit, aka MMU, matches, or maps this virtual adress into a page table entry, that contains valid-invqlid bit, to check if the memory is allocated to this process or not. when not, the interacts creates a singal to inform the cpu of the problem, then a page fault handler is created. 

the virtual adress space contains of chunk of fixed sized spaces, called the pages, that is used both in flat and multi level paging. 
