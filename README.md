# FPC/Lazarus cross-platform VirtualBox Appliance
A VirtualBox Appliance for cross-platform FreePascal/Lazarus development

Quickly and easily get going with Lazarus and FPC, already set up with useful packages and ready for cross-compilation.

## Installing
* Open VirtualBox
* File menu -> Import Appliance
* Select the .ova file and follow the instructions
* Enjoy your shiny new VM

## User
The username is "developer" and the default password is "fpc".

You should change the password after adding the virtual machine.

## Get going
* Start the VM
* Double click the Lazarus icon
* Write code

## Compilers
* Linux x64
* Windows x64
* macOS x64 (Darwin)

## Debugger
* GDB

## Extra packages installed:
* cryptolib4pascal (Crypto)
* hashlib4pascal (Hashing)
* lazbarcodes (Barcodes)
* pascaltz (Timezones)
* xmailer (Email)
* OPM (Online Package Manager)
* anchordockingdsgn 1.0 (Single Lazarus window)

## Tested
I created a Lazarus project and added a button which shows some text when clicked.

It is set up with build modes for Linux, Windows, and macOS as examples.

The output path is set up as bin/$(TargetOS)/helloworld to generate executables for each platform in a separate folder.

After compiling for Windows I transferred and ran the executable on my Windows host machine to make sure cross compilation was successful.

## FPCUpDeluxe
Installing FPC and Lazarus was done with FPCUpDeluxe, which I left on the image for easy updates.
