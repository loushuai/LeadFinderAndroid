# AndroidLeakFinder
This tool is used to find resource leaks in Android programs, espacially in NDK codes.

## Compile

$cd LeakFinderAndroid
$ndk-build

## How To Use
* You should have a rooted andoird devices
* Disable SELINUX: <br>
> $setenforce 0
* set preload: <br>
> $setprop wraper.yourappname LD_PRELOAD=libmemleak.so
* run your app.
* use ps commond to find your app's pid.
* send signal to show check result on shell: <br>
> $kill pid -SIGUSR2

## Filter
Sometimes there are too many useless infomation caused by JVM in the result.
You can filter the result with keywords. <br>
> $echo "keyword" >> /data/local/tmp/memleakconfig.txt
