# UCC

##### This was built for the students of schools/colleges that still use TurboC++ and teach it's archaic code samples, and ask its students to use the same. You no longer need to torture your eyes by using that ugly blue and old pixelated IDE anymore, and the codes you write will be exactly same as TurboC++! No 'using namespace std;' stuff required!

*NOTE: This can compile and run both C and C++ codes and has FULL support for the graphics library.*

*NOTE: a UCC workspace is a folder that contains all your working files and folders for UCC. Make sure you don't use the folder for anything else.*

#### Common Instructions:
*EVERY* valid UCC Workspace will contain these folders:
- `builds/` (this will contain the built EXE files)
- `sources/` (this will contain the C/CPP source code)
- `logs/` (this will contain the build and DosBox logs)
- `files/` (this will contain the files created through C/C++ using filestreams)
- `headers/` (this will contain your custom header files)

### WINDOWS:

*Here is a video that guides you on how to install Visual Studio Code (a very good code editor) and use it with UCC:* https://www.youtube.com/watch?v=WLkYAsEskq8

#### *Instructions:*
1. **DOWNLOAD UCC:** https://github.com/uditkarode/ucc/archive/refs/heads/windows.zip
2. Now, make a new folder somewhere, and extract the zip inside it.
3. After extraction, **you must run** `UCC-INIT.bat`. The file will set up the directory and automatically remove itself.
4. After this step, you **must** place your source codes in the sources/ directory.

You can now use `UCC-BUILD.bat`, `UCC-RUN.bat`, or `UCC-BUILD-RUN.bat` to compile, run, or compile and seamlessly run respectively.

This has been tested working on Windows 10.


*For advanced users:*
If you prefer direct command line usage, you can change directory to the assets folder and use ucc this way:
```bash
.\bash ucc --build abc.cpp
.\bash ucc --run abc.cpp.EXE

--OR--

.\bash ucc -br abc.cpp
```

### LINIX/UNIX:

ARCH LINUX/MANJARO USERS:
  
##### UCC is available on the AUR.  
`yay/yaourt -S ucc`  
  
###### SCRIPT METHOD:

##### The commands below will do the heavylifting for you. You can copy and paste them to your terminal directly. After executing them, your workspace will be ~/UCCRoot :

```bash
cd ~
git clone --depth 1 https://github.com/uditkarode/ucc.git
sudo mv ucc/ucc /bin/ucc
sudo chmod +x /bin/ucc
mkdir UCCRoot && cd UCCRoot
mv ~/ucc/BIN .
mkdir builds sources logs files headers
rm -rf ~/ucc
ucc --workspace .
```

You can now place your source code in the ~/UCCRoot/sources directory.

After setting up UCC, you can compile and run your programs with a command as simple as `ucc -br program.cpp`!

For instructions on usage of the script, use `ucc --help`

In the words of Bob the Builder:
> Happy Building!

## UCC Commands:

Usage: ucc [option] [argument]

ucc -b/--build <filename>: builds <filename> from the sources folder.
  
ucc -r/--run <filename>: runs <filename> from the builds folder.
  
ucc -br/--build-run <filename>: builds and runs <filename> from sources folder.
  
ucc -cb/--c-boilerplate <filename>: places <filename> in sources folder with C boilerplate.
  
ucc -cpb/--cpp-boilerplate <filename>: places <filename> in sources folder with CPP boilerplate.
