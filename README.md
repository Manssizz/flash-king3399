## Mengubah firmware King3399 dengan rkdeveloptool linux
Image bisa ambil dari repository ophub (https://github.com/ophub)

### Bahan
- install rkdeveloptool (https://wiki.radxa.com/Rock3/install/rockchip-flash-tools)
- download loader (https://github.com/Manssizz/flash-king3399/blob/main/rk3399_loader_v1.27.126.bin)
- download fw

### Steps
- Colok usb type C ke device
- Tekan tombol reset sebelum colok power
- jalankan perintah dibawah

```
#### Cek device
sudo rkdeveloptool ld

#### Hapus bootloader
sudo rkdeveloptool db rk3399_loader_v1.27.126.bin

#### Flash image
sudo rkdeveloptool wl 0x0 <image.img>

#### Reset device
sudo rkdeveloptool rd
```

> Apabila tidak terdeteksi atau terkena maskroom saat `rkdeveloptool ld`, jumper pin **resistor** dan **grounding** yang ada digambar lalu colok power

![maskrom-pin](https://github.com/Manssizz/flash-king3399/assets/23637327/71923adb-c540-4024-996d-bcc99272c2dd)
