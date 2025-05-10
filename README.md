# Firefly Logged Pi Image
This repo and its .img.xz output contains only the elements for 
Firefly Field Day Logger that are used for the installer media
of the "turnkey"  Pi appliance. In general, any issues
with FFDL should be filed at 
[Firefly Logger](https://github.com/jxmx/firefly-logger)

## Assembling the FFDL Pi Image
Assembly of the FFDL Pi Image is done with the `build-image` script. It's 
runnable from any system supported by CustomPiOS by simply running
`build-image -v VERSION`. 

One of the SLOWEST parts of the job is compressing back down the image file
with `xz`. The `build-image` script is optmized to use `xz -T0` which will use
all available cores/threads to compress the file. Thus making the assmebly
faster is literally throwing more CPUs at the process. 
