# GeForceNow Exploitation - a little writeup 



## disclaimer
all of this was tested in NVIDIA GEForce Now Version 1.8.2.17/po (EU Central).
I will only release the cmd.exe and admin exploit, its an LPE btw, if NVIDIA Doesn't contact me with any of their technicans, or securty officers,´, or something like that. No, I won't fill a normal form to report this as a bug.
## Restrictions
the task which scans for any malicious program, has been found out to be explorer_fake.exe, with the default PID 2788. 
If you stop the explorer_fake.exe you can make "start explorer.exe", to start the default explorer.
Restricted programs, which will crash NVIDIA GeForce now, with reporter key: 0x80030015:
- explorer.exe
- netsh lan/wlan
## Vulnerabilities
- Script injection and malicious program running by iSn0w \
      - This script injection vuln. leaded me to starting cmd and other exe programs from anywhere, as well as reading, and                                              writng to almost all locations.
- Program execution by JohnVS \
      - based on macro keys, he was able to run cmd as well as a powershell on the main system. read and write.
## Error codes
There are bunch of reporter keys, which appear, when NVIDIA GeForceNow was either crashed, or you were kicked out of your session.
- 0x80030015 \
      - This reportey key, comes up, when after the program detected that a program from the restricted list was started.
        You can see the restricted list above.
- 0x4010002 \
      - This error code means the GeForce NOW app is unable to find a graphics processing unit (GPU) capable of decoding the        video format used by GeForce NOW.








# To contribrutors
If you know any other reporter keys, just make a pull request and throw them into the Error codes section
