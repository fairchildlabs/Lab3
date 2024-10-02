# Lab3

## 3.1 Enable the Wired Network interface on your PI

```
$ sudo nano /etc/network/interfaces.d/eth0

** paste these lines

allow-hotplug eth0
iface eth0 inet static
address 11.11.11.1/24
netmask 255.255.255.0
gateway 11.11.11.1

<CTRL><X> then "Y" to save

$ sudo nano reboot

```

## 3.2 Use Ethernet (Network) Cable to attach LABPC to PI

Disable Network Connection on PI (DEMO)
Start Putty normally. (Alternate, use 11.11.11.1 IP address)

## 3.3 Create /mnt direcotry for USB

```
$ sudo nano /etc/fstab
** This makes sure that the usb drive is always at /mnt
** Paste this line
/dev/sda1	/mnt	auto	defaults,nofail,sync	0	0
<CTRL><X> and "Y" to exit

$ mount -a

** This creates a link so you can view files on the USB drive from browser
$ sudo mkdir /var/www/html/usb
$ ln -s /mnt /var/www/html/usb




















ffmpeg -f v4l2 -framerate 60 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -c:v copy 1.mov
ffmpeg -f v4l2 -framerate 60 -video_size 1920x1080 -c:v yuyv422 -i /dev/video0 -c:v copy 1.mp4
ffmpeg -f v4l2 -framerate 60 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -c:v mjpeg 2.mp4

ffmpeg -f v4l2 -framerate 60 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -preset faster -pix_fmt yuv420p 5.mp4

ffmpeg -f v4l2 -framerate 60 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -preset faster -pix_fmt yuv420p /var/www/html/7.mp4
ffmpeg -f v4l2 -framerate 30 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -preset faster -pix_fmt yuv420p /var/www/html/7.mp4


ffmpeg -f v4l2  -hwaccel drm -framerate 30 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -preset faster -pix_fmt yuv420p /var/www/html/7.mp4


ffmpeg -f v4l2 -framerate 30 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -preset faster -pix_fmt h264_v4l2m2m /var/www/html/77.mp4

-i /dev/video0 -preset faster -pix_fmt yuv420p %s", fr, szRes, fn);

ffmpeg -f v4l2 -framerate 60 -video_size 1920x1080 -c:v mjpeg -i /dev/video0 -c:v h264_v4l2m2m 33.mp4

ffmpeg -y -input_format yuyv422 -i /dev/video0 -an -s 1920x1080 -r 30 -vcodec h264_v4l2m2m -num_output_buffers 32 -num_capture_buffers 16 -b:v 6M -pix_fmt nv12 -f mp4 output1.mp4
ffmpeg -i /dev/video0 -vcodec h264_v4l2m2m -pix_fmt nv12 64b.mp4

