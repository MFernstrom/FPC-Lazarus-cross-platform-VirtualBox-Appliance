# FPC/Lazarus cross-platform VirtualBox Appliance
A VirtualBox Appliance for cross-platform FreePascal/Lazarus development

This VirtualBox Appliance is already set up with FreePascal, Lazarus, several cross-compilers, useful packages, and VirtualBox Guest Additions.

## Installing
* Download the OVA file here: http://www.mediafire.com/file/v8y6vlyelgd1s46/Lubuntu_FreePascal_and_Lazarus.ova/file (I uploaded it on Mediafire as it's too large for GitHub at 4.5gb)
* Open VirtualBox
* `File` menu -> `Import Appliance`
* Select the .ova file and follow the instructions
* Enjoy your shiny new VM

## User
Username is `developer` and the password is `fpc`

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

## How to set up your own project for cross-compilation

### Create a new build mode
* Open `Project` -> `Project Options` in the top menu
* Click on `Compiler Options` in the left-hand list
* Click on the button with the three dots at the top, next to "Build modes"
* Double click on the name of the build mode to edit it
* Change it to `Linux`
* Click the `+` sign on the left in the new window
* Edit the new modes name and make it Windows
* Click on the `OK` button

### Change compilation target for the build mode
* In your `Project Options` click on `Compiler Options` in the left-hand list
* Pick the `Build Mode` to edit from the dropdown at the top
* Click on `Config and Target` in the left-hand menu
* Change the `Target OS` to fit your target, such as `Win64` for 64-bit Windows, or `Linux`
* Change the `Target CPU` Family to fit your target, such as `x86_64` for 64-bit systems
* Click OK at the bottom

### Setting Project Path
* Click on Paths in the left-hand menu
* Change the Target file name to something like `bin/$(TargetOS)/myapp` this will create a folder for the specific OS when compiling

### Compiling for a specific target
On the Lazarus IDE coolbar menu, there's an icon that loos like cog with a wrench, it has a dropdown arrow.
* Click on the dropdown arrow to pick any of your `Build Modes`
* Use `Run` -> `Build` or `Run` -> `Compile` as you usually do

## About the Appliance
The base image is a Lubuntu install, which is a light-weight Ubuntu distro. It was set up using VirtualBox 6.1.16r

## Tested
I created a Lazarus project and added a button which shows some text when clicked.

It is set up with build modes for Linux, Windows, and macOS as examples.

The output path is set up as bin/$(TargetOS)/helloworld to generate executables for each platform in a separate folder.

After compiling for Windows I transferred and ran the executable on my Windows host machine to make sure cross compilation was successful.

## FPCUpDeluxe
Installing FPC and Lazarus was done with FPCUpDeluxe, which I left on the image for easy updates.
