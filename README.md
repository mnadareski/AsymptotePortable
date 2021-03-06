-----------------
Asymptote Portable:
-----------------
Developed for the PortableApps.com Platform

This is a PortableApps.com packaging of the descriptive vector graphics language Asymptote.

-----------------
Release Log:
-----------------
2.24 Dev Test 1:
- Uses Asymptote 2.24 as a base
- Relies on GSview Portable (http://portableapps.com/node/38391)
- For standalone running:
	+ Compiled xasy to Windows binaries using py2exe (http://www.py2exe.org/)
	+ Settings are stored in Data\configs\xasy.conf
	+ Has to move to the user directory during runtime, for now
- For referenced running:
	+ Calling AsymptotePortable.exe with parameters uses asy.exe instead
	+ User-defined runtime settings are stored in Data\configs\config.asy
	+ Stays in Data directory during runtime
- Other usage and options have not been explored
	+ Documentation mentions using gsview from PATH
	+ May be codependent on other items
- Known issues:
	+ Closing xasy is not enough, command window has to be closed separately
	+ xasy can crash if it does not draw from a premade file
	+ Both seem to be there in original python version as well, to an extent
	+ Outputted .eps files are stored in App\asy
		= Cannot be moved because GSview is called immediately
- Installer size: 8.43 MB
- MD5 Hash: 71356364e28868dea0839553b9bc4f4c

2.24 Dev Test 2:
- Started transition to commandline-only interface
	+ Commented out references to xasy in launcher
	+ Moved all xasy runtime files to separate folder as optional install
	+ No direct way to launch xasy without modifying launcher.ini
	+ Made commandline program asy.exe be default regardless of how called
- Installer size: 8.42 MB
- MD5 Hash: c43fd9cbe286262cdfcf891fd0872c02

2.24 Dev Test 3:
- Commented out WorkingDirectory
	+ Caused issues with integration testing
	+ All outputted files should move to appropriate folders
- Installer size: 8.42 MB
- MD5 Hash: 04aabd0636ba7c1c83db9680d52005f4

2.24 Dev Test 4:
- Fixed spelling error in launcher.ini
	+ All environment variables should work now
	+ Thanks to d4winds for all external work put into this
- Installer size: 8.42 MB
- MD5 Hash: a932f443024d608b273895194577a6ef

2.24 Dev Test 5:
- Updated registry items taken care of
- Completely removed WorkingDirectory by default
- Added new environment variables for futureproofing
- Installer size: 8.42 MB
- MD5 Hash: fa9671ae11442f01b2a65b987828a757