These are the Config.h and Config_adv.h files for the Ender 5 3D printer under Marlin 2.0.x.  
This is compiled and running on the Creality 1.1.5 silent board and has also been tested to work on the 1.1.4 board.  
  
The currently enabled/disabled features are:  
  
- Disabled Bootscreen (reclaim memory space)  
- Disabled Status Screen Image (this remove "Ender-5" from the top left corner)  
- Enabled S-Curve Acceleration & Junction Deviation @ 0.08 (please check tutorials and change as needed for your use case)
- Linear Advance Supported. To make the use of Linear Advance, you will need to do the calibration, then add M900 K## to Slicer's Custom Starting G-Code.  
- Disabled Speaker  
- Disabled ARC Support (It's for laser etching, reclaim memory space)  
- Boosted Buffer for improved print quality with Octopi, almost as good as printing from SD Card  
- Set print bed to 220x220 with the volume of 300   
- Enabled Manual Mesh Bed Leveling  
- #define MESH_BED_LEVELING  
- ** TO DO ** Enable Restore Leveling Data after G28 (for mesh leveling) - Right now I just use M420 S1 after G28  
- Enabled LCD Bed Leveling Menu  
- Disabled Status Message Scrolling (reclaim memory space)  
- Disabled Long Filename Scrolling (reclaim memory space)  
  
I took the long list of items from https://github.com/firestrife23/ender-5-marlin and pared it down to the above items.    

To save some space and possibly enable other features you can follow his complete listing of changes.  
