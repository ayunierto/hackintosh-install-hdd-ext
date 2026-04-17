# hackintosh-install-hdd-ext

```bash
# 1. Mapear el archivo .raw como si fuera un disco
sudo losetup -fP imagen_olarila.raw

# 2. Identificar la partición de instalación (usualmente la p2)
lsblk -f

# 3. Volcar SOLO esa partición al disco físico
sudo dd if=/dev/loop0p2 of=/dev/sda6 bs=4M status=progress
```
