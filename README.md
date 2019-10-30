# code-snippets
Various scripts and code snippets

# Convert-WindowsImage.ps1
Built on the (outdated) Technet Gallery script to be found here: https://gallery.technet.microsoft.com/scriptcenter/Convert-WindowsImageps1-0fe23a8f

Supports as an example Windows 10 WIM to VHD(X).

Example: 
1. Get Windows Image details from source to convert:
```
Get-WindowsImaeg -ImagePath '.\Windows 10.wim'
```
You will need ImageName parameter of the image in scope for the next step (example: myImage).

2. Convert the image by running the below code to have it compatible with a Hyper-V Gen1 VM:
```
Convert-WindowsImage -SourcePath '.\Windows 10.wim' -VHDFormat VHD -VHDPath .\Win10.vhd -Edition 'myImage' -VHDPartitionStyle MBR -Verbose
```
