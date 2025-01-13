## Open a Command Prompt(Terminal).
 ** { Windows key + X, then select it from the menu. }
## OR
  ** { Windows key + R, then type in CMD & press Enter. } **

## Type diskpart and press Enter.

## Type list disk to see all disks connected to your computer.
  Identify the USB Disk: You can unplug it and type list disk again, reconnect it and repeat to determine which disk is your USB drive.
  Note the disk number corresponding to your USB drive.

## Select the USB Disk: (_the number will be relative to the local enviroment_)
  If disk number is disk 2
  Type select disk = 2

# After prompt confirming your selection
## Type clean into the terminal
## Next type convert mbr
# Finally type create partition primary

That's it, now go and format your USB drive in your file explorer.
