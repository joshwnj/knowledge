# erase a cdrw

I had to erase a CD-RW in MacOs today, and Disk Utility was not giving an option to do it. Finally found there's a way to do it via command line. Even better!

```
drutil -drive 1 erase quick
```

There's also the option to use `full` instead of `quick`. Not 100% sure what that means, I guess maybe you want it if there is any sensitive data on the CD.
