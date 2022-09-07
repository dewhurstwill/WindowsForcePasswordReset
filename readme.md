1. Build a windows install USB
2. Boot from USB
3. Press `SHIFT + F10`
4. Run the following commands in order

```
diskpart
list disk
select disk # (where # is the disk you want)
detail disk (to see partitions)
select volume # (where # is the volume you want)
assign letter=x (where x is the drive letter)
exit
x: (where x is the drive letter)
cd x:\Windows\System32 (where x is the drive letter)
copy Utilman.exe Utilman1.exe
del Utilman.exe
copy cmd.exe Utilman.exe
```

5. Restart the device
6. Open the Utility manager on the login screen
7. Run the following commands in order

```
net user x * (where x is the username you wish to change the password)
net user x /expire=NEVER
del Utilman.exe
ren Utilman1.exe Utilman.exe
```

Should work on all versions of visons including windows 11
