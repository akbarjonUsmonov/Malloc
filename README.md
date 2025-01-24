# Welcome to My Malloc
***

## Description
    In this project, we will use the heap by recreating our own implementation of malloc(). But what is malloc? Malloc is a dynamic memory allocator — it gives you a block of memory on the heap during run time. You want to use malloc when you don’t know the memory size during compile time. It’s also useful when you need to allocate memory greater than the size of the stack. More commonly, malloc is used for objects that must exist beyond the scope of the current block.

## Installation
    To run this project use GNU compilation command or Makefile that i provided
        $> make
## Usage
    Code to test:
        #include <unistd.h>
        #include <stdio.h>
        #include <sys/mman.h>
        #include <string.h>

        void* my_malloc(int size) {
        return mmap(0, size, PROT_READ | PROT_WRITE, MAP_ANON | MAP_PRIVATE, -1, 0);;
        }


        int main(int ac, char **av) {
            char *src = "hello";
            char *dest = my_malloc(strlen(src) + 1);


            strcpy(dest, src);
            printf("s\n", dest);
            return 0;
        }

### The Core Team
Akbar Usmonov\
<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px' /></span>
