### **RePatcher:**


**RePatcher** is a native desktop app that generates new presets for instruments, effects, and Players in **Reason**. RePatcher is inspired by the random patch generation tools created by Ekssperimental Sounds. Analysis and generation run locally on your computer. The installed official Reason Rack Plugin (RRP) supplies device authorization and read-only access to factory presets. RePatcher uses VST3 on Windows and tries VST3 first on macOS, with AU as a fallback. It does not work with the standalone Reason DAW or the AAX version of RRP. The installed and authorized VST3/AU RRP is a requirement for this app to function.


### **Finding devices and building generators:**

Open **Installed devices \> Scan for updates**. RePatcher asks the RRP which installed devices are authorized for the current session, then matches them against the analyses saved in its local database. On Windows, opening Installed devices starts a background RRP session that RePatcher reuses until you close the app.

For devices that use the `.repatch` format, including built-ins such as Europa, one shared analyzer reads the factory preset information into memory. It looks for settings that vary, discrete choices such as waveform selectors, and controls that tend to move together. It takes category labels from preset metadata, factory folders, or recognizable words in patch names. The current analyzer needs at least **two distinct usable settings** for a factory-based generator. A folder-based category generally needs **eight** to stand on its own. The local database retains the derived model and scan status. Factory preset files stay with the installed Rack Extension (RE) and are never directly copied by RePatcher.

**Analyze** previews the categories for one device so you can rename them and choose which to add. Bulk analysis adds categories automatically. **Analyze Saved Presets** can build custom categories from a folder containing presets for multiple devices and add them alongside existing categories. When factory data is insufficient and a usable control schema is available, RePatcher offers **Random Exposed Controls**. It varies five controls per patch by default, caps that count at the number of controls available available, and keeps an identifiable primary output at its default. Random Exposed Controls can be used even if a suitable model has been built, though results are less likely to be usable.


### **Generating a pack:**

Choose a device, pack type, and patch count. **Mixed** balances the available preset categories. For example, if you select Leads and Pads for a pack of ten, you get five of each. For a factory-based category, RePatcher draws new settings from the learned ranges and uses the learned relationships to keep related controls in plausible combinations. Where it can identify level controls, it nudges them toward typical settings for that category. This is a fast estimate based on parameters. Actual playback loudness can still vary.

Preset names combine two to four words randomly from category-specific lists and a shared vocabulary. Names are unique within each pack, with a numeric suffix available as a last resort. **Character** summarizes what the generator did. It can show the category and factory preset count, the number of randomized controls, or traits inferred from the settings of a built-in device. Reusing the same seed, generator, and pack settings reproduces the pack.


### **Exporting to Reason:**

**Save ZIP** puts presets in category folders. RePatcher writes `.repatch` files directly. Built-ins with dedicated formats, such as Subtractor and Thor, use device-specific formats that require Reason’s native writer and are encoded through the installed RRP. Sample-based patches can point to assets already installed with the device or in Reason’s included factory sound banks. When a pack needs special placement for Reason’s browser to recognize its categories, the ZIP includes `INSTALL.txt` with macOS and Windows instructions.


### **Supplemental:**

This app was created using what is currently referred to as "vibe coding" methods using Codex. Even though this is a simple utility app, the creation process involved several decisions, design points, and iterations. The build process used an Apple Silicon Mac for its development environment, along with the full version of Reason 14\. It was also tested against Reason 14 for Windows, and Reason Free 14 on a Mac. This app may work with v12 and v13 of Reason, but it has not been tested against those versions.

This app was tested across a large range of first- and third-party REs. However, the app can only be tested against personally-owned REs. The app has been designed to be algorithmically generic to hopefully cover the widest range of REs as possible, as long as they use the `.repatch` format (which nearly all do). Untested REs and those created after this release may still encounter issues or produce unusable patches.

Note: On macOS, you may receive a warning from Gatekeeper when launching. After the first launch, you can prevent this by going to System Settings \> Privacy & Security \> Security \> Allow.

Obligatory: This app is not affiliated with or endorsed by Reason Studios.

Please let me know if you encounter any major issues or have feature/usability ideas. Thank you\!
