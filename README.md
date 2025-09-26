the goal here is to identify the different types of files on these SD cards
these are configuration files from quantum Q-Logic 3 power wheelchairs

each card is placed into the joystick and automatically configures the chair for the connected components on the next power-up
(power seating, type of motors used, max speed ratings, motor compensation etc)

when components on the chairs are changed (like adding power seating or swapping to faster motors) the SD cards configure the chair's modules, and then are left in the chair.

if the card is later removed however, the configuration will remain on the control modules in the chair.  

these are a 'one shot' type programming setup, but are intended to be LEFT IN the joystick
in other words, it doesnt need to reference these SD card configuration files on EVERY bootup.  (it still might do this - but is unknown right now)

we want to figure out which files reference which functions so that a library/catalog can be built, and files can be picked thru to create custom configurations WITHOUT relying on DME's and manufacturers
to make changes on the chairs.  

after configuration has been completed (and just in general) on every powerup the chairs looks for an FAT32 formatted micro SD card to be present. if a card is NOT present, the chair will throw an error
(but after a short delay the chair will continue to function normally without an SD card present)
the SD card can be EMPTY when this check happens, and there will be NO error

other unknowns:
1) does chair SEARCH/COMPARE  SD card contents for NEW configurations on every bootup?
2) after a successful configuration change, does the chair write an identifier to the card? or somehow otherwise invalidate the card for future use?

assumption: the root of the SD card has a 'directory' file that is refrenced for quick comparison, and directs to other files on the card if reconfiguration is required

there are currently 4 micro SD cards uploaded here, and they have NEVER been connected to a chair

(and a 5th 'used' sd card from a chair with an unknown cofiguration)

soon i will be connecting (copies of) them to a chair, and uploading the cards again after a configuration change has completed to see if there are any differences
