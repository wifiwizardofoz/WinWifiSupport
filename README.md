# WinWifiSupport
A simple Microsoft Windows command to determine a Wi-Fi adaptor's key capabilities

**Author:** Brett Verney</br>
**Version:** v0.1 | 6-08-2020

## Background
There are a number of key technologies&nbsp;that, if supported by a Wi-Fi adaptor may be explicitly enabled on the supporting Wi-Fi infrastructure. By filtering the ```netsh wlan show``` command we can outpout the key information that we require, without having to sift through all of the data.

## Command
```netsh&nbsp;wlan show all | findstr /c:"Firmware Version" /c:"DOT11k" /c:"Transition" /c:"MU-MIMO" /c:"Spatial Streams" /c:"Management Frames" /c:"Driver                    :" /c:"Vendor  " /c:"Provider" /c:"Date" /c:"Version                   :" /c:"Radio types"```

## Output

You should see something similar to this:

![WinWifiSupport Output](https://github.com/wifiwizardofoz/WinWifiSupport/blob/master/winWifiSupport.PNG)
