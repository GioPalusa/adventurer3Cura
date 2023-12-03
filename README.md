# Cura settings for Flashforge Adventurer 3

Installation Instructions

Install Cura and launch it. Cura will prompt you to add a printer. Pick any one, the default is fine.

Add the X3GWriter plugin from the Marketplace menu item. Quit Cura.

Find the location of the Cura configuration folder. You can press "Help" and then "Show configuration folder"

The files must be extracted/added into the same folder names (definitions & extruders) as they are located here.

Launch Cura and add the printer(s) by selecting from the menu "Preferences ==> Configure Cura... ==> Printers ==> Add ==> Add a non-networked printer" - scroll down to "Flashforge" and expand it.

Happy slicing!



# Manual setup from within Cura
Here are settings if you want to add the standard Flashforge printer that comes with Cura and then change the settings:

## Step 1: Launch Cura 

## Step 2: Add Your 3D Printer 
### 2.1 Option 1: 
Settings -> Printer -> Add Printer 

### Option 2: 
On the main interface click the Printer section then click Add printer in the dropdown. 

### 2.2 
On the pop-up window please find Flashforge in the left list then fill in your Printer name on the right. Click Add to proceed. 

### 2.3 
On the Machine Settings window fill in the Printer spec as suggested below. Then click Next to proceed. 

#### Printer Setting 
- X (Width) 150.0
- Y (Depth) 150.0
- Z (Height) 150.0
- Build plate shape: Rectangular 
- Original at Center √
- Hotend bed √
- G-code flavor Marlin 

#### Printhead Setting 
- X min -20 
- Y min -10 
- X max 10 
- Y max 10 
- Gantry Height 150.0
- Number of Extruders 1
- Apply Extruder Offsets to GCode √

#### Start G-code:
````
G28
M132 X Y Z A B
G1 Z50.000 F420
G161 X Y F3300
M7 T0
M6 T0
M651 S255
````

#### End G-code：
````
M104 S0 T0
M140 S0 T0
G162 Z F1800
G28 X Y
M132 X Y A B
M652
G91
M18
````

#### Nozzle Settings 
- Compatible material diameter 1.75 
- Nozzle offset X 0.0
- Nozzle offset Y 0.0
- Cooling fan number 0

## Step 3: Select Nozzle Size 
Once the printer is added you may go to Settings -> Extruder 1 -> Nozzle Size to select your printer’s nozzle size as 0.4mm. 

## Step 4: 
You may now create new project and start slicing 
