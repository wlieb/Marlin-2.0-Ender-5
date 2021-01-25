These are the Config.h and Config_adv.h files for the Ender 5 3D printer under Marlin 2.0.7.2  
This is compiled and running on the BTT SKR Mini E3 v1.2 with 3D Touch Probe (BL Touch Clone)  
  
This firmware should capture most of the Ender 5 settings.

As always some modifications will need to be made to account for your own touch probe offsets, linear advance, junction deviation, etc...

Items changed from stock Marlin 2.0.7.2 confiuration.h:

- Added Custom Bootscreen
- Added Machine Name
- Baud Rate 115200
- #define MOTHERBOARD BOARD_BTT_SKR_MINI_E3_V1_2
- #define SERIAL_PORT 2
- #define TEMP_SENSOR_BED 1
- #define BED_MAXTEMP      125
- Enabled #define PID_EDIT_MENU
- Enabled #define PID_AUTOTUNE_MENU 
- Modified PID_PARAMS:
   #else // Creality Ender-5
    #define DEFAULT_Kp  21.73
    #define DEFAULT_Ki   1.54
    #define DEFAULT_Kd 76.55
  #endif
- Enabled #define USE_ZMIN_PLUG
- Enabled #define USE_XMAX_PLUG
- Enabled #define USE_YMAX_PLUG
- Disabled #define USE_XMIN_PLUG
- Disabled #define USE_YMIN_PLUG
- Enabled and changed X, Y, Z, and E0 Driver Type to TMC2209
- Modified #define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 400, 93 }
- Modified #define DEFAULT_MAX_FEEDRATE          { 300, 300, 5, 25 }
- Modified #define DEFAULT_MAX_ACCELERATION      { 500, 500, 100, 5000 }
- Modified #define DEFAULT_ACCELERATION          500    
- Modified #define DEFAULT_RETRACT_ACCELERATION  500   
- Modified #define DEFAULT_TRAVEL_ACCELERATION   500
- Modified #define JUNCTION_DEVIATION_MM 0.08
- Enabled #define S_CURVE_ACCELERATION
- Enabled #define USE_PROBE_FOR_Z_HOMING (BL TOUCH)
- Enabled #define BLTOUCH (BL TOUCH)
- Enabled and modified #define NOZZLE_TO_PROBE_OFFSET { -42.5, -11.5, -2.71 }  (BL TOUCH)
- Modified #define XY_PROBE_SPEED 12000 //(133*60) (BL TOUCH)
- Enabled #define Z_MIN_PROBE_REPEATABILITY_TEST (BL TOUCH)
- Disabled #define DISABLE_INACTIVE_EXTRUDER
- Modified #define INVERT_X_DIR true
- Modified #define INVERT_Z_DIR true
- Modified #define INVERT_E0_DIR true
- Modified #define X_HOME_DIR 1
- Modified #define Y_HOME_DIR 1
- Modified #define X_BED_SIZE 235
- Modified #define Y_BED_SIZE 235
- Modified #define Z_MAX_POS 300
- Enabled #define AUTO_BED_LEVELING_BILINEAR (BL TOUCH)
- Enabled #define RESTORE_LEVELING_AFTER_G28 (BL TOUCH)
- Modified #define GRID_MAX_POINTS_X 5 (BL TOUCH)
- Enabled #define EXTRAPOLATE_BEYOND_GRID (BL TOUCH)
- Enabled #define ABL_BILINEAR_SUBDIVISION (BL TOUCH)
- Enabled #define LEVEL_BED_CORNERS
- Enabled #define Z_SAFE_HOMING (BL TOUCH)
- Modified #define HOMING_FEEDRATE_XY (25*60)
- Enabled #define EEPROM_SETTINGS
- Enabled #define EEPROM_AUTO_INIT 
- Modified #define PREHEAT_1_TEMP_HOTEND 220  (Hardened Steel Nozzle)
- Modified #define PREHEAT_1_TEMP_BED     60
- Modified #define PREHEAT_1_FAN_SPEED   255
- Modified #define PREHEAT_2_TEMP_HOTEND 250
- Enabled #define PRINTCOUNTER
- Modified #define DISPLAY_CHARSET_HD44780 WESTERN
- Enabled #define SDSUPPORT
- Enabled #define SD_CHECK_AND_RETRY
- Enabled #define INDIVIDUAL_AXIS_HOMING_MENU
- Enabled #define CR10_STOCKDISPLAY
- Enabled #define FAN_SOFT_PWM

Items changed from stock Marlin 2.0.7.2 confiuration_adv.h:

- Enabled #define QUICK_HOME
- Enabled #define PROBE_OFFSET_WIZARD
- Enabled #define LCD_INFO_MENU
- Enabled #define STATUS_MESSAGE_SCROLLING
- Enabled #define LCD_SET_PROGRESS_MANUALLY
- Modified #define SD_FINISHED_RELEASECOMMAND "M84XYE"
- Enabled #define POWER_LOSS_RECOVERY
- Enabled #define POWER_LOSS_PURGE_LEN   20
- Enabled #define POWER_LOSS_RETRACT_LEN 10
- Enabled  #define LONG_FILENAME_HOST_SUPPORT
- Enabled #define SCROLL_LONG_FILENAMES
- Enabled #define BABYSTEPPING
- Enabled #define DOUBLECLICK_FOR_Z_BABYSTEPPING
- Modified #define X_CURRENT       580 
- Modified #define Y_CURRENT       580
- Modified #define Z_CURRENT       580
- Modified #define E0_CURRENT      650
- Enabled #define SQUARE_WAVE_STEPPING
- Enabled #define TMC_DEBUG
