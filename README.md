Quantavex
=========
This project aims to be a modified version of Firefox, with a distinct identity and high customization capability.

Build
-----
This project is built on top of the esr153 branch from the official Firefox repository.

To build your own copy:

1. Clone Firefox from the correct branch:
```
git clone --branch esr153 https://github.com/mozilla-firefox/firefox.git
cd firefox
```
-patches
2. Apply the patch:
```
git am /path/to/quantavex/*.patch
```

3. Build the project by running these commands from the project root after applying the patch:
```
cd browser/extensions/newtab && npm run bundle
cd ../../.. && ./mach build faster && ./mach run
```
