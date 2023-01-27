# [stb-image-frpf2](https://github.com/ImageProcessing-ElectronicPublications/stb-image-frpf2) demo

The image is scaled using "Find Replicant Pixel Fast".

## Origin

![orig](images/butterfly.png)

---

---

### Upsampling x2

```shell
stbimfrpf2 butterfly.png butterfly.x2frpf2.png 
```
```log 
Load: butterfly.png
image: 256x256:3
process: downsample
process: gradient
process: FRPF2
Save png: butterfly.x2frpf2.png
```

![x2](images/butterfly.x2frpf2.png)

### Upsampling x4

```shell
stbimfrpf2 butterfly.x2frpf2.png butterfly.x4frpf2.png 
```
```log 
Load: butterfly.x2frpf2.png
image: 256x256:3
process: downsample
process: gradient
process: FRPF2
Save png: butterfly.x4frpf2.png
```

![x4](images/butterfly.x4frpf2.png)

## Compare

### Bicubic

```shell
stbresize -r 4 butterfly.png butterfly.x4cubic.png
```
```log 
Load: butterfly.png
image: 256x256:3
resize: 1024x1024:3
method: bicubic
Save png: butterfly.x4cubic.png
```

![x4c](images/butterfly.x4cubic.png)

### FRP2 (long!!!)

```shell
stbimfrp2 butterfly.png butterfly.x2frp2.png 
```
```log 
Load: butterfly.png
image: 256x256:3
process: downsample
process: gradient
process: FRP2
Save png: butterfly.x2frp2.png
```
```shell
stbimfrp2 butterfly.x2frp2.png butterfly.x4frp2.png 
```
```log 
Load: butterfly.x2frp2.png
image: 256x256:3
process: downsample
process: gradient
process: FRP2
Save png: butterfly.x4frp2.png
```

![x4l](images/butterfly.x4frp2.png)

---

---

