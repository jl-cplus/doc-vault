# Chrome/Chromium segmentation fault with GTK4

## Description
Running Chrome/Chromium on GNOME (Wayland) with GTK4 installed results in a segmentation fault  

```
$ chromium  
Segmentation fault (core dumped) chromium  
```
> [!NOTE]  
> Chromium 147.0.7727.101 (Official Build) Arch Linux (64-bit)    

### Workaround
Launch Chrome/Chromium with GTK3  

```
$ chromium --gtk-version=3  
```

### Related Issues
1. Chromium bug tracker: [40277125](https://issues.chromium.org/issues/40277125)  
