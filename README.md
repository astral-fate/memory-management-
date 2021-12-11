# memory-management-

previously, we said that the os is responsible to manage the hardware components. 
one of these components is how much the process (program under execution) can use the actual 
physical memory. 

the os manages the memory by allocating a virtual adress space for every procces, and that adress includes the details; heap, stack and data of this process.
then the os, with the help of the memory management unit, aka MMU, matches, or maps this virtual adress into a page table entry, that contains valid-invalid bit, to check if the memory is allocated to this process or not. when not, the interacts creates a singal to inform the cpu of the problem, then a page fault handler is created. 

the virtual adress space contains of chunk of fixed sized spaces, called the pages, that is used both in flat and multi level paging. 

the mmu, uses the page entry table to:
preform the translation from virtual to physical address 
 every procces tables contains a context switch, to switch the virtual adress space to a valid page, and mmu uses it to establish a validity access
 
 
 If the mmu, the hardware components determines that a physical memory access cannot be performed, it causes a page fault.
18the access is illegal, because the memory adress that is requested has not been allocated at all. since the memory adress translation happens on pretty much every memory reference. most memory management units would integrate a small cache of valid virtual to physical adress translation. 


21thr presence of a TLB will make the entire translation process much faster. it will also imply what kinds of pages can be there. 
 
 
 
 the mmu hardware integrates a hardware cache that's dedicated for caching address translation, and this cache is called Translation Look Aside Buffer, or TLB.
 
access to preform the translation. 



mathematical examples on page size, page table and number of entries, and page table size. 



 A process with 12 bit addresses has an address bthe address space will only the 1st 2KB and the last 1KB are allocated and used how many entries are there in a single level format
 
 
 
 
 
 
  How many entries are needed in the inner page tables of the 2 level page table when the 2nd format is used
  
  
  
  
  
 
