## Tasmota and Sonoff NSPanel

### Quixk early version of TFT custom screen firmware upload

Copy the nextion.bs file to your device with the File System Manager. Change the autoexec.bs to load that instead of the nspanl.bs if you were using that with custom screen firmware.

https://github.com/peepshow-21/openhab/blob/main/nextion.be

Download the jar file and run it with an installed java runtime on your windows or linux host

https://github.com/peepshow-21/openhab/blob/main/ns-flash.jar

Browse to the TFT file you want to upload.
Select the folder you want the chunk files to to. It's best to make this a folder that is seen by your local http server. But you can put them anyway and move the after.
Press 'Build'. It will split the TFT into files tamsota can load

Boot the NSPanel with the new nextion.bs loaded.
At the console, type;

FlashNextion http://192.168.1.100:8080/static/chunks

Where this is the place the chunk files live.

That's it. then just wait. The display should show install progress.


