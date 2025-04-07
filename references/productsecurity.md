

Product Security
================


## Secure boot

### Binaries/Executables and instructions in Binaries

Binary (Binaries) can also be called executables. These contain complete software that makes a product work as expected are stored in memory (Though not exactly SD Card...can consider as SD Card for storing photos, documents,...).

Binaries are considered as packages of series of 0s and 1s representing instructions for CPU. Instructions are statements telling CPU what needs to be done (like read a number from a memory location, another number from another memory location, add the two numbers, store the sum into another memory location). 

When these instructions are executed by CPU, the intended functionality of the product is realized. For example, instructions in binaries in TV when executed realizes the functionality of TV and users can select the videos and watch them along with audio in TV. Similarly, mobile phones (When instructions in binaries in TV when executed realizes the functionality of mobile phone).

Though, here, binary is explained as software for the complete product, binary can be individual software components like application that runs on already functional product. For example, already functional mobile phone can download an application and new functionality is introduced in the product/Mobile phone. This individual application can also be called as binary. Some more such individual software components will be mentioned.

### Initial binary (InitBoot) that starts the boot process

InitBoot binary is stored in a memory location that is very secure (That is almost sure that no one can hack). Notice that it is mentioned as "almost sure" as from the perspective of security, it is never mentioned that "complete secure" as hackers may find a way to hack). The contents of InitBoot can be accessed by CPU and the instructions specified in InitBoot can be executed by the CPU.

When product is powered on, CPU executes the instructions in InitBoot memory area. **This is where secure boot process starts. These instructions ask CPU to verify the contents of another binary called bootloader whether they are authentic or not (For this, md5 checksum check, CRC check, digital signature checks are used) md5 checksum, CRC check, digital signature checks need to be studied separately. At this stage, these can be considered as mechanisms to ascertain that the binaries are not modified (by hackers or due to some error). This check is important to ensure that the execution of instructions in the binaries will not lead to malfunctioning of the product**. Once this check is done successfully (**if any modification is detected in binaries, boot process is aborted**), InitBoot binary will have instructions to copy contents bootloader to memory location that can be accessed by CPU and instructions copied there can be executed by the CPU.


### Bootloader

Bootloader is another binary that helps in making a product work. Bootloader is stored in a memory location (as explained above, though it is exactly not SD Card, consider it as SD Card for easy understanding).

Based on instructions in InitBoot memory area, contents/instructions of bootloader binary are copied to memory location where instructions can be executed by CPU. After copy is done, instructions of bootloader binary are executed.

Bootloader continues to initialize hardware - CPU, memory and other aspects which can be learnt later. Apart from this, CPU continues execution of instructions of bootloader that makes the product function completely. **Key functionality that is relevant to secure boot is the instructions in bootloader checks the authenticity of subsequent software components/binaries that gets loaded and executed**.


## Different types of attacks

* Buffer overflow attack
* Denial of Service attack
* Network based attacks (Man in the Middle, Replay,...)
* Hardware based attacks (Physical tampering, Fault injection ....)




## Secure Communication

### Cryptography (Encryption, Decryption)

#### Different types of cryptography algorithms

Asymmetric cryptography: RSA, ECC, DSA, DH 

symmetric cryptography: AES, DES, 

Hash functions: MD5, CRC,...






## Hardware security



## Secure Development Lifecycle

### Secure programming languages

Characteristics of a programming language that makes them secure - Memory safety, Strong type,...

Rust, Go, Python,.... comparison of these programming languages

### Threat Modelling

### Penetration testing


