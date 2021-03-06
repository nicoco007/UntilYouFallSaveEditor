# Until You Fall Save Editor
This small program allows you to export/import save data as JSON files.

### ⚠️ Use this program at your own risk! I am not responsible for loss of save data. Back up your saves before messing with them!

## Getting Started
### Installing the Mod
First, you need to get the encryption keys from the game. You can do this however you want &ndash; the main program accepts them as hexadecimal strings &ndash; but I've built a simple plugin/mod that works under both [BepInEx](https://github.com/BepInEx/BepInEx) and [MelonLoader](https://github.com/LavaGang/MelonLoader) to make things easier.

#### BepInEx
Download the [latest build of the plugin for BepInEx](https://nightly.link/nicoco007/UntilYouFall-SaveEditor/workflows/build/main/AesKeyExtractorPlugin-BepInEx.zip) and extract the DLL into the `BepInEx\plugins` folder inside your game's install folder. Note that you must also have [JSON.NET (Newtonsoft.Json)](https://www.newtonsoft.com/json) installed &ndash; if you don't, download [the latest release](https://github.com/JamesNK/Newtonsoft.Json/releases/latest) and put `Newtonsoft.Json.dll` in the `BepInEx\plugins` folder.

#### MelonLoader
Download the [latest build of the plugin for MelonLoader](https://nightly.link/nicoco007/UntilYouFall-SaveEditor/workflows/build/main/AesKeyExtractorPlugin-MelonLoader.zip) and extract the DLL into the `Mods` folder inside your game's install folder.

### Extracting the keys
Once the mod is installed, simply launch the game and a new file called `SaveEncryptionKeys.json` should be created in the game's root folder.

### Using the Program
Download [the latest version of the program](https://nightly.link/nicoco007/UntilYouFall-SaveEditor/workflows/build/main/SaveEditor.zip) and extract it wherever you want. You may need to also download and install the [.NET Desktop Runtime 5](https://dotnet.microsoft.com/download/dotnet/5.0) for the program to run properly.

When you run it for the first time, it should automatically detect the location of your saves. If it doesn't, you will be prompted by a message asking you to locate them. They are usually in the folder `C:\Users\<your username>\AppData\LocalLow\Schell Games\UntilYouFall`. Make sure you select the `UntilYouFall` folder and not one of the folders inside it!

![Main Window](https://i.imgur.com/m4ri2Wi.png)

Once that's done, press the "Import Key & IV..." button to open the file generated by the mod earlier. It should fill in the "Encryption Key" and "Encryption IV" boxes.

Values in the save files are stored as strings even if they are objects or numbers. The "Deserialize Values" checkbox enables/disables deserializing these values into their actual JSON representation.

Your preferences will be saved to a file called `settings.json` (folder/keys/checkbox) next to the executable.
