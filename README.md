# VcvRackVSFiles

JSON files for working with VCV Rack and plugins in Visual Studio 2019/2022, using its "Open Folder" functionality.

### Get started

* Put the three JSON files into your plugin development directory.
* Adjust the paths and version numbers in the files according to your MinGW and VCV Rack installations.
* Open your plugin development directory in Visual Studio, either in VS via File -> Open -> Folder or from the File Explorer via right-click -> "Open with Visual Studio".

### Benefits

* You now have full Intellisense support from VS for gcc's standard libraries, Rack's sources and your plugin's sources.
* In VS's Solution Explorer, the following commands are available via right-click:
	* On the root folder: Open in MinGW console
	* On any *.cpp file: Compile
	* On the Makefile: All the make commands (make, clean, rebuild, dep, dist, install, run) and an addditional "Run Rack" command (the installed one, not in debug mode)
* Note that these commands are blocking. That is, you can't start another command while the previous one is still running.
* From the "Select startup item" dropdown, select the "gdb Rack" entry and press the green arrow to run. This gives you full VS debugger support including breakpoints, variable watch etc. for your plugins and Rack itself.

Feel free to modify the files according to your requirements. Bear in mind though that this system is very fickle and documentation is very sparse or even misleading. Even small changes might break things.
