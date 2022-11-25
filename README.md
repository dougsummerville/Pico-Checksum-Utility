# Pico Checksum Utility
 A tool to add a CRC32 to an Pi Pico ELF file.

Python script that reads a 32-bit ELF file compiled for the Pi Pico and adds a CRC32 to the stage 2 boot section at physical address 0x10000000.  Assumes the section is already padded to 256 bytes.

In a C bare metal environment, the Pico SDK method of extracting the stage2 boot code as assembler data directives does not permit the linker to resolve symbols. Doing it after the link stage allows more flexibility in writing stage 2 boot code.
