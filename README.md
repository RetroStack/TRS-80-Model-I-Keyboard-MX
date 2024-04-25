# TRS-80 Model 1 - MX Keyboard

This project is a reimplementation of the original keyboard of the iconic TRS-80 Model 1 computer. My revision is designed to replicate the functionality of the original but using modern "OEM" MX style keycaps. The entire project is available under the MIT license.

![E2 Replica](/Latest/TRS80_Model_I_Keyboard_MX_E2_Photo.png)
(Style to resemble the original keyboard)

## Project Details

The project consists of multiple parts, each with its own source files, example ordering process, and consecutive assembly.

The parts are:
- PCB
- Custom Keycaps
- Shield
- 3D printed parts (LED standoff and optional bezels)

The Assembly Guide is coming soon.

## PCB

The PCB has been implemented using KiCAD 7. The KiCAD project files are included in this repository.

![E2 Replica Front](/Latest/TRS80_Model_I_Keyboard_MX_E2_3D_Front.png)
![E2 Replica Back](/Latest/TRS80_Model_I_Keyboard_MX_E2_3D_Back.png)

In the "Latest" folder, you'll find the most up-to-date design files, including:

- Gerber files suitable for popular online PCB manufacturers like [PCBWay](/Latest/TRS80_Model_I_Keyboard_MX_E2_Gerber_PCBWay.zip) and [JLCPCB](/Latest/TRS80_Model_I_Keyboard_MX_E2_Gerber_JLCPCB.zip). Most manufacturers should be fine with either.
- A Bill of Materials (BOM) in [PDF](/Latest/TRS80_Model_I_Keyboard_MX_E2_BOM.pdf) format.
- The [full schematics](/Latest/TRS80_Model_I_Keyboard_MX_E2_Schematics.pdf) of the E2 revision.

### RetroStack Libraries

To work with this KiCAD project, you'll need the RetroStack libraries for KiCAD. Please [follow this link](https://www.github.com/RetroStack/KiCAD-Libraries) to access and install these libraries.

### Supported Key Switches

This PCB supports both, the PCB mounted as well as the plate mounted MX-style key switches.

![Supported Key Switches](/Images/Various_Switches.png)

Hole to cover both are provided on the PCB:

![Footprint Holes in PCB](/Images/Keyswitch_Footprint.png)


## Keycaps

A template of keycaps is provided to resemble the original keycap design closely.

- Keycap template in [Illustrator (.ai) format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Keycap_Template.ai)
- Keycap template in [SVG format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Keycap_Template.svg)

These templates should work with most keycap manufacturers.

To simplify the ordering process, I've provided an additional template for MaxKeyboard.com. See the example order instructions below.

### Keycap Order Instructions - MaxKeyboard.com

Go to: [MaxKeyboard](https://www.maxkeyboard.com/iso-layout-custom-color-cherry-mx-keycap-set-top-print-blank.html)
(If URL doesn't work anymore, select the ISO layout keycap set for MX from the store with custom prints on top.)

On the page, select the following:
- Select “105” (ISO 105-key (FULL SIZE) +US$5.00)
- Select “6.0” (6.0x Unit Spacebar)
- Select “A” (Top Print +US$15.00)
- Select “NO I have my own” (if you don’t want a keycap puller)
- Select “I will upload my print file (+US$10.00)”
- Upload the file at “Upload Your Artwork” (get the correct template to upload [here](/Latest/TRS80_Model_I_Keyboard_MX_E2_105_6.0X_TOP_PRINT_COLOR_KEY.ai))
- Add a comment “Please do not use homing keys!”

The last comment is optional, but it will make sure that you do not have these "bumps" in specific keys (e.g. see the "F" and "J" key of a modern standard keyboard). These are not on the original keyboard.

This set of keycap will cost about US$55 without tax and shipping (early 2024).

NOTE: Some of the following steps were already defined in the template file, but the website is not clear if it needs to be redefined. Just to be safe, follow the next steps as well.

What is left is the overall color design in the “DESCRIPTION” section at the bottom of the page:
- For 1. Bottom Row, select “6.0x Spacebar Row”
- For 2. Keycap Color, select the color “Black” (first) and select “All Keys”. Then, select “beige”(4th) (white is too bright and beige fits better in my opinion), and click on the keys which should be white (I marked them in the preview picture above). Select the most right “Reset” key and click “red”. The template has a few repeated keys each with a different color scheme. This gives you the opportunity later to choose the one which you like the most.
- For 3. Alphanumeric, leave everything as-is
- For 4. Modifiers, leave everything as-is
- For 5. OS Key, leave everything as-is
- For 6. Text Color, click “white” (2nd) and “All Keys”. Then select one white keycap and click “black” (1st), and select all other white keycaps. (Probably not needed, but just in case!)
- Add checkmark at “I confirm that the layout is correct”

At the end, the preview will look something like this:

![Keycap Preview](/Images/Order_Color.png)

It is correct that you can't see the labeling in this preview. That is provided in the template above and will not be applied to the preview you see.

Finally, scroll up and click “Add To Cart”.

You can customize the keycap colors, but be aware what the text color is sometimes white and other times black. Here is a preview with label color for reference:

![Keycap Selection](/Images/Keyboard_Preview.png)

## Shield

The shield is different to the original keyboard shield.

## Customizability

Since there was an opportunity to improve upon the keyboard, I provided various ways to optionally customize your keyboard.

### Additional Keys

Modern keyboards generally use 6 units (6u) wide spacebars (or similar short sizes) instead of the 8 units (8u) the original Model I keyboard used. This replacement keyboard comes with a 6 units wide spacebar, which means that there is additional space next to the spacebar for two additional keys to fill the gap of the original keyboard bezel.

![Full Keyboard with additional keys](/Images/Variations/Full_Keyboard_Additional_Keys.png)

Any key can be mapped to these two additional keys by selecting the row and column:

![Keyboard Mapper](/Images/Keyboard_Mapper.png)

On the underside, you can add DIP switches (or simply use jumpers) to select the row and column:

![Custom Mapping](/Images/Custom_Mapping_Additional_Keys.png)

### Remap other Keys

You can also remap the BREAK and CLEAR keys to anything you want:

![Custom Clear and Break](/Images/Key_Mapping_Break_Clear.png)

### Add Reset Key

To emulate a popular Model 3 & 4 keyboard feature, the ability to add a reset key is provided:

![Reset Key](/Images/Variations/Full_Keyboard_Reset_Key.png)

Simply add a jumper to the keyboard:

![Keyboard Jumper](/Images/Keyboard_Reset_Jumper.png)

Then, connect to a via close to the Reset circuity on the main board:

![Mainboard Jumper](/Images/Main_PCB_Reset_Jumper.png)

![Connected Keyboard](/Images/Connected_Reset_Jumper.png)

### Keycap Variations

As each keycap set consists of 105 keys. The basic keyboard without numpad requires only 53 keys while with numpad it only needs 65 keys. Even with the additional 2 keys, we need at most 67 keys. There are 38 keys left (minus some unused key sizes and shapes), which can be duplicated. I've provided a few variations of keycaps in different colors, but also custom prints (like the CTRL key for "Electric Pencil"):

![Keycap Selection](/Images/Keyboard_Preview.png)

This provides a couple of variations (and more):

![Keyboard with additional keys](/Images/Variations/Full_Keyboard_Additional_Light_Keys.png)
![Keyboard with additional keys](/Images/Variations/Full_Keyboard_Light_Numbers.png)
![Keyboard with additional keys](/Images/Variations/Full_Keyboard_Red_Break.png)
![Keyboard with additional keys](/Images/Variations/Keyboard_Light_Keys.png)





## Main TRS-80 Model 1 Repository

For additional resources related to the TRS-80 Model 1, be sure to check out the central page for the TRS-80 Model 1 on RetroStack. You can find it [here](https://www.github.com/RetroStack/TRS-80-Model-I).

## Support this Project

RetroStack is passionate about exploring and preserving the legacy of older computer systems. My work involves creating detailed documentation and videos to share the knowledge. I am also dedicated to reviving these classic systems by reimplementing them and offering replacement parts at no cost. If you're keen on supporting this unique project, I invite you to visit my [Patreon page](https://www.patreon.com/RetroStack). Your support would be immensely valuable and greatly appreciated!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
