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


the presence of a TLB will make the entire translation process much faster. it will also imply what kinds of pages can be there. 
 
 
 
 the mmu hardware integrates a hardware cache that's dedicated for caching address translation, and this cache is called Translation Look Aside Buffer, or TLB.
 
access to preform the translation. 



mathematical examples on page size, page table and number of entries, and page table size. 




![FGW0o6wXIAUCAfn jpeg](https://user-images.githubusercontent.com/63984422/145692077-816beb22-dcde-4e9d-b79e-410ea95a86b4.jpg)


 A process with 12 bit addresses has an address space where only the 1st 2KB and the last 1KB are allocated and used how many entries are there in a single level format
 
 
 we have 12 bits, and that can be written as 2^12. 
 then we have 6 offset bits, that is 2^6
 
and we know that:

virtual adress space bits = number of pages x size of pages 

hence, to find the number of pages, which equals the number of entries on the page table:


number of pages = bits/size

hence 

2^12/2^6=2^6
= 64
 
 
 
 
 
 
 
 
 
 
 
 ![FGW0o6wXIAUCAfn jpeg-١](https://user-images.githubusercontent.com/63984422/145692087-e09d6a8b-3dab-49e1-9b7c-864e78cfdbf1.jpg)

 
 
  How many entries are needed in the inner page tables of the 2 level page table when the 2nd format is used
  
  
  the size of this adress is the same; 2^6
  
  and now since we have two pages, an inner page that is not used, and an outer page which has the value of 4 bits,  then we represent this number by the power of 2, hence it becomes 
  
  2^4 = 16
   
   
   and since we have three segments then:
   
   16×3= 48 bits
  
  
  
  
  
  
  
  another mathematical example
  
  
  Consider a memory architecture using two-level paging for address translation. 
The format of the virtual address, physical address, and PTE (page table entry) 
are below: 

![Screenshot_٢٠٢١١٢١٢-٠٠٣٧٢٧_OneDrive](https://user-images.githubusercontent.com/63984422/145692466-60184f51-73e3-4774-8cc9-1e32ab9dbac6.jpg)





(a) What is the size of a page?



(b) What is the size of the maximum physical memory?







(c) What is the total memory needed for storing all page tables of a process that 
uses the entire physical memory
  
 
