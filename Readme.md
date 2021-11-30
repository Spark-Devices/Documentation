<h3  align="center">This is a guide for how to build the official verision of Spark-OS</h3>

### Guide for maintainers

- First step is to check  [the official devices repository](https://raw.githubusercontent.com/Spark-Devices/Documentation/fire/devices) and add your device if it is not present .

- Required props are for official maintainers : 

> ro.spark.device.name=Poco F3  <br>
> ro.spark.group.url=https://t.me/ <br> 
> ro.spark.maintainer=Sukeerat Singh Goindi <br>
> ro.spark.maintainer.username=irongfly <br>

Please add these props in your device repos.

*1st line: Device name  <br> 
2nd line: Telegram device group link <br>
3rd line: Your full name <br>
4th line: Your telegram username* <br>

- Always push your device trees with the naming scheme like **android_XXX** and with with correct branch.
- Track everything needed in vendor/ci

> Kernel -
> android_kernel_xiaomi_alioth
> <br> DT - 
> android_device_xiaomi_alioth
> <br>  DT Common -
> android_device_xiaomi_alioth-common
> <br>  Vendor Common  - 
> android_vendor_xiaomi_alioth-common
> <br>

- Now for dependencies , they should all be on Spark-Devices  
- Note :- If you add a directory to be synced which already exists , please use vendor/ci/codename.sh (For Examples Hals
- Now for patches or source changes you might need you can push to [Code Review System](https://review.spark-os.live) and cherry-pick in the same file.
- For user builds , export buildtype="user" in ci repo.sh
