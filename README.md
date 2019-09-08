# GeForce Now Exploitation - a little writeup 

## Code generation algorithm
theres a algorithm the code, for the beta tester phase gets gernerated in. i will link it here, as soon as i write a little writeup.
untile then you can use https://www.joseph.sh/geforce/

## Disclaimer
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
There are bunch of reporter keys, which appear when NVIDIA GeForceNow terminates the session.

| Error Code | Description                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| 0x80030015 | GFN detected that a program from the restricted list was started                                                             |
| 0x4010002  | GeForce NOW app is unable to find a graphics processing unit (GPU) capable of decoding the video format used by GeForce NOW  |
| 0x000001F9 | Launching many sessions at once or too quickly (rate limit)                                                                  |
| 0x80030017 | Right clicking on most filetypes                                                                                             |

#### Files you can right click without getting terminated
* Images
* cmd.exe

#### Unblocked programs
* Paint
* DxDiag
* cmd.exe

#### Blocked programs
Pretty much anything that is not on the list above is blocked.

## For the LULZ

Here is a screenshot of VSCode running on the GFN server 😎
![img of code](/screenshots/vscode.jpg)


# To contribrutors
If you know any other reporter keys, just make a pull request and throw them into the Error codes section
