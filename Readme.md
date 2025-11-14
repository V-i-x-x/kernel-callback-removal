# Kernel Callbacks Removal (Bypassing EDR Detections)

## Warning
Even though you can download the binaries from the `releases`, you have to make sure that the offsets and the binary search opcodes done is the same on your windows version or you will get a **BLUE SCREEN OF DEATH**

## Offsets and Patterns Modification
All offsets and patterns that needs to be modified based on your windows version can be found in the file ending with `Util.h` within each project.

Following the guide inside the folder will help you figure it out how to retrieve the opcodes and offsets.

** Each subsection contains a readme with instructions**

## New Undisclosed Technique 
I discovered an alternative method that bypasses kernel-level verification by overwriting the callback function inside the Callback entry itself with a KCFG-compliant function that simply returns. This evades detections that monitor changes at the callback array level `(For Kernel Notify Routines Callbacks)`.

## Prerequisistes

This is an advanced topic requiring the following prerequisites:

- Assembly understanding

- Familiarity with C programming

- Experience with WinDbg

- Familiarity with IDA

- Windows kernel exploitation knowledge

## Tools Used

WinDbg: [Windows Debugging Tools](https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/)

IDA: [Hex-Rays IDA Free](https://hex-rays.com/ida-free)

## Kernel Debugging Setup

To debug your local kernel (for fixing your offsets and reversing), follow the instructions here: [Setting up local kernel debugging](https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/setting-up-local-kernel-debugging-of-a-single-computer-manually)

## Target Audience

This project is for both pentesters and defenders to understand how attackers can bypass EDR kernel implementations.

## Purpose

- For everyone to be able to learn how technically bypassing EDR is done.
- For having the flexibility to create your own tool which make it pretty easier to bypass signature based detection.
- For researchers to be able to play around the code and debug and reverse.

## Techniques Covered

- Kernel Notify Routines Callback Bypass
- MiniFilter File Callback Bypass
- Network Callout Callback Bypass
- ETW-TI Kernel Bypass

## Tested on
Host Name:                     WIN11

OS Name:                       Microsoft Windows 11 Pro

OS Version:                    10.0.26100 N/A Build 26100

### Disclaimer
This project is for **educational purposes only**. Unauthorized use of this tool in production or against systems without explicit permission is strictly prohibited.
