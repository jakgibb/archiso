Modified version of djgera's build scripts.
These changes are to suite my personal needs so they are unlikely to benefit you.

## build.sh modified to allow:

### Alternative cache location:  
My archiso build system (which itself is a version created by these scripts) is booted to RAM and the build directory is located on an external HDD.  
As the system is booeted into RAM, this means the system disk is limited to the amount of free RAM %.   
To prevent the system running out of memory, the cache directory to be a 'tmp' directory the build scripts location on a HDD.  
This may differ depending on where the external HDD is mounted, so modified build.sh  
to accomdate the changing mount point.  
  
### Removed 'run_once' from various functions:  
Allows adding/updating files from airootfs to the work directory and building a
new ISO without having to run the entire build script process.
