We were given two binaries with zero imports, a pretty common obfuscation technique used by real-life malwares

![ss](https://user-images.githubusercontent.com/46635361/51080312-c6300800-16e1-11e9-8e79-6ab54bce4d9a.png)

upload Mal_1.exe to [hybrid-analysis.com](hybrid-analysis.com/sample/42512f779a32d5e677e534ad87524e886a80572c2de4e47ed993e264735b31ba)

there are 4 Extraced files one of them named config.vbe which is a [vbs compailed script](https://fileinfo.com/extension/vbe)

![extracted_files](https://user-images.githubusercontent.com/46635361/51080022-7b5fc180-16dc-11e9-8ad6-3d643b5cb37c.png)

and the malware will delete itself at some point using powershell 

![untitled](https://user-images.githubusercontent.com/46635361/51080134-b662f480-16de-11e9-9e01-566b8f14c003.png)

now let's get the extracted files ourselves .. open up your win7 debugging vm and just use any file monitor tool i used Moo0, then run the binary.

![s](https://user-images.githubusercontent.com/46635361/51080067-a1399600-16dd-11e9-9c09-9644c2c71c43.png)

locate and decode config.vbe using  decode-vbe.py

![decode_vbe](https://user-images.githubusercontent.com/46635361/51080078-ce864400-16dd-11e9-8f34-3c3998fcaf19.png)

the same vbs script can be found within hybrid-analysis report too.

![untitled](https://user-images.githubusercontent.com/46635361/51080092-291fa000-16de-11e9-8e9e-10e53d0fe102.png)

