# Install Manjaro on your HackberryPi4B

First Download and flash the image from [Manjaro web](https://manjaro.org/products/download/arm?device=Raspberry+Pi+4B/400/3B%2B/3B/Zero+2)
Copy and paste the following lines into the `/boot/config.txt`  

```sh
dtoverlay=vc4-kms-v3d
dtoverlay=vc4-kms-dpi-hyperpixel4sq
```

Insert the TF card, and then you can see the HackberryPi now running Manjaro
![image](https://github.com/user-attachments/assets/ee96315a-e1d8-47ed-91a3-77d8391af5c3)
