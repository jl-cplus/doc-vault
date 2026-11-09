# LUKS Cheatsheet  
  
> [!IMPORTANT]  
> This cheatsheet covers adding, changing, removing, and viewing passphrases for LUKS-encrypted devices using `cryptsetup`.  
  
> [!TIP]  
> Use `lsblk` and `awk` to identify encrypted device paths  
>  
> **Example Output:**  
> /dev/nvme0n1p2  
> /dev/sda2  
```bash
$ lsblk -nrpo NAME,FSTYPE | awk '$2 == "crypto_LUKS" {print $1}'   
```
  
> [!NOTE]  
> The `--force-password` option bypasses the configured password quality checks.  
    
### Add (New Passphrase)  
Add an additional passphrase without removing any existing passphrases.  
```bash
$ sudo cryptsetup --force-password luksAddKey <encrypted_device_path>  
```
  
### Change (Existing Passphrase)  
Replace an existing passphrase with a new one.   
```bash
$ sudo cryptsetup --force-password luksChangeKey <encrypted_device_path>  
```
   
### Remove (Delete Passphrase)  
Remove an existing passphrase.  
```bash
$ sudo cryptsetup luksRemoveKey <encrypted_device_path>  
```
> [!CAUTION]  
> Before removing a passphrase, ensure that at least one other valid passphrase exists and has been tested successfully.  
  
### Inspect (View Information)  
Display the LUKS header information, including keyslot status.  
```bash
$ sudo cryptsetup luksDump <encrypted_device_path>  
```
  
### Verify (Test Passphrase)  
Verify a passphrase without opening the encrypted device.  
```bash
$ sudo cryptsetup open --test-passphrase <encrypted_device_path>  
```
