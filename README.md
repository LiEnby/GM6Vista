# GM6-Vista

What is this repo? 
- Patched executables for GameMaker 6 and 6.1a to allow it to run on Microsoft Windows Vista, and later versions

What this is NOT:
- This is NOT a crack or keygen for GameMaker 6.0, or 6.1a, the pathced version still requires a valid GM6 or GM61a product key to unlock all features

How to apply the patch?
- Simply [Download the patch](https://github.com/KuromeSan/GM6Vista/releases/latest) for whatever version your using and extract the 7z file using 7-zip, 
then copy the files "Game Maker.exe" and "rundata" into the install directory of GameMaker 6


Technical details:
OK, so the only reason why GameMaker 6.0, 6.1, and 6.1a dont run under modern versions of windows is: they were packed using ASProtect 1.3 

ASProtect is [Executable Packer](https://en.wikipedia.org/wiki/Executable_compression) and a [Digital Rights Management](https://en.wikipedia.org/wiki/Digital_rights_management) designed to make it hard to [Reverse Engineer](https://en.wikipedia.org/wiki/Reverse_engineering) and or tamper with executable files- to make it harder to crack or something.

these old versions of ASProtect stopped working with Windows Vista, because of its use of [Self Modifying Code](https://en.wikipedia.org/wiki/Self-modifying_code) 
because the GameMaker 6 main executable *and* game executables are packed with it, all GM6 games simply stopped working on all versions of windows, after Vista.

This patch simply removes ASProtect from the main executable, and runner executable & changes rundata validiation checks to match new data. 
it also patches some hard coded offsets into the rundata executable for changing icons.

the rundata used here is the same one given to us by Mark Overmas in the GM6 to Vista converter, which is basically just the original rundata executable, (pre-packing) however as we dont have the original unpacked main executable, i had to use some unpacker tool .

NOTE: this patch makes no changes to the license checks, the engine still requires a valid GM6 product key!
