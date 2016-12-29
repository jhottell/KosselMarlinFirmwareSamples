# KosselMarlinFirmwareSamples
Sample configurations to get Marlin Firmware up and running fast on Kossel 3D printers using Ramps electronics. These instructions should get you started for ANY delta 3D printer!

I have a video describing setting up and calibrating your Kossel Mini or Kossel XL for the very first time! 
http://www.electronhacks.com/2016/12/diy-kossel-xl-reprap-3d-printer-build/


Quick start instructions as seen in the video
Software to Download
Arduino IDE     - For loading Firmware and USB drivers          - https://www.arduino.cc/
SketchUp Make   - For creating 3D STL files                     - http://www.sketchup.com/download
NetFabb Basic   - For repairing broken STL files                - https://github.com/3DprintFIT/netfabb-basic-download/releases
Repetier-Host   - For slicing, manual control, and printing     - https://www.repetier.com/
Marlin Firmware - Arduino machine Firmware                      - https://github.com/MarlinFirmware/Marlin
Calibration Objects - For calibration...                        - http://www.thingiverse.com/thing:5573  

Other Firmware
Repetier-Firmware - Good marlin alternative firmware but not used for this tutorial - https://www.repetier.com/

Websites
Thingiverse - Online repository where people share their 3D files   - http://www.thingiverse.com/
Electronhacks - My Blog with info, downloads, links, and videos     - http://www.electronhacks.com/2016/12/diy-kossel-xl-reprap-3d-printer-build/
Stepps per MM calculator -                                          - http://www.prusaprinters.org/calculator/#stepspermmbelt

Here are my printer settings along with line numbers. Your printer will probably be a little different.

My Kossel Mini Settings:
125 BAUDRATE                    250000
132 MOTHERBOARD                 BOARD_RAMPS_14_EFB
381 EXTRUDE_MINTEMP             10  - I like to circumvent the cold extrusion safety measure
426 #define DELTA
438 DELTA_DIAGONAL_ROD          213
441 DELTA_SMOOTH_ROD_OFFSET     164
444 DELTA_EFFECTOR_OFFSET       31
447 DELTA_CARRIAGE_OFFSET       27
    Printable Radius            127  - Not used in Marlin Firmware
453 DELTA_PRINTABLE_RADIUS      90
484 USE_XMAX_PLUG
485 USE_YMAX_PLUG
486 USE_ZMAX_PLUG
537 DEFAULT_AXIS_STEPS_PER_UNIT { 80, 80, 80, 890 }
580 Z Probe Options             No Z probe for me
885 AUTO_BED_LEVELING           No Auto Bed leveling for me
964 MANUAL_Z_HOME_POS           245.2
982 HOMING_FEEDRATE             100*60



My Kossel XL Settings:
120 BAUDRATE                    250000
127 MOTHERBOARD                 BOARD_RAMPS_14_EFB
381 EXTRUDE_MINTEMP             10  - I like to circumvent the cold extrusion safety measure
426 #define DELTA
438 DELTA_DIAGONAL_ROD          320
441 DELTA_SMOOTH_ROD_OFFSET     202
444 DELTA_EFFECTOR_OFFSET       24
447 DELTA_CARRIAGE_OFFSET       22
521 XYZ_FULL_STEPS_PER_ROTATION 400
522 XYZ_MICROSTEPS 16
523 XYZ_BELT_PITCH 2
524 XYZ_PULLEY_TEETH 16
450 DELTA_RADIUS                181
453 DELTA_PRINTABLE_RADIUS      135
484 USE_XMAX_PLUG
485 USE_YMAX_PLUG
486 USE_ZMAX_PLUG
545 DEFAULT_AXIS_STEPS_PER_UNIT { XYZ_STEPS, XYZ_STEPS, XYZ_STEPS, 650 }
580 Z Probe Options             No Z probe for me
885 AUTO_BED_LEVELING           No Auto Bed leveling for me
975 MANUAL_Z_HOME_POS           245.2
982 HOMING_FEEDRATE             60*60
