py2app-pyqt-codesign-fix-os-x
=============================

Currently if you're building with py2app, any Qt Frameworks will fail to sign inside the package.

Fix your py2app binary that is using Qt4 or 5 to be able to codesign it and put it up in the app store or be opened in yosemite. 

Steps:

	1. Change the path to your app file inside of `prepare_for_codesign.py`
	2. Run `python prepare_for_codesign.py`
	3. Codesign the file `codesign --deep --verbose -s "Developer ID" ./path/to/Your.app`

