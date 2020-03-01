# How to delete Apps that can't be deleted on Android.

## Prerequisite
1. ADB install
You need ADB(Android Debug Bridge) is included in the Android SDK platform tools package. This package can be downloaded using the SDK Manager and is installed in android_sdk/platform-tools/ (<https://developer.android.com/studio/releases/platform-tools?hl=ko>).  

2. Activate phone developer settings

## Steps
### 1. Open CMD
In my case, adb.exe is installed in <C:\Users\A\AppData\Local\Android\Sdk\platform-tools>  
Open CMD in here.

### 2. Find your device
```>adb devices```  

you can see your device connected your computer.  
you will see like the following picture.  
![adb devices](https://user-images.githubusercontent.com/34882947/75626690-f5b71200-5c0c-11ea-9e33-7a397aacc4df.JPG)

### 3. Delete
#### 1. You need to know the package name of the app you want to delete.
So how to know the app package name?
> download APK inspector (<https://play.google.com/store/apps/details?id=com.ubqsoft.sec01>)  
> then, execute the APK inspector app. you choose an app to want to know the app package name.  

you will see like the following picture.  
![APK name](https://user-images.githubusercontent.com/34882947/75626713-43337f00-5c0d-11ea-8280-fa1c17a3605d.JPG){: width="500" height="500"}

#### 2. Delete the app
```
>adb shell
$pm uninstall -k --user 0 {name of package}
```
![adb delete](https://user-images.githubusercontent.com/34882947/75626796-f308ec80-5c0d-11ea-9026-76acc00302ca.JPG)