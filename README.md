# TRS-80 Model 1 - MX Keyboard

This project is a reimplementation of the original keyboard of the iconic TRS-80 Model 1 computer. My revision is designed to replicate the functionality of the original but using modern OEM MX style keycaps. The entire project is available under the MIT license.

![E2 Replica](/Latest/TRS80_Model_I_Keyboard_MX_E2_Photo.png)
(Style to resemble original keyboard)

## Customizability

As modern keyboards generally only use 6 units wide spacebars (6u) instead of the original 8 units (8u) the Model I used, these set of keycaps are also only 6 units wide. That means that there is space next to the spacebar for two additional keys to fill the gap of the original keyboard bezel.

When initially surveyed which keys should be put in place, I received a variety of opinions. I, therefore, opted to make this completely customizable:
- on the PCB - by providing the ability to set jumpers onto every row and column of the keyboard matrix to select any key, including missing ones like the "Ctrl" key for the electric pencil program.
- on the shield - by providing additional holes
- as keycaps - by providing a variety of different colors and additional keycaps that were not there originally (e.g. "Ctrl" keycap)

Additionally, I made the "Clear" and "Break" switches customizable as well. By default, they work as originally intended, but by cutting the trace between two solder jumper pads, you are able to provide jumpers between row and column for these keys as well.

An additional key was also provided through the jumpers: a reset key. This makes it possible to control the systems reset switch that usually is on the back (inside) the case, but is now available on the keyboard itself. To make this work, only one jumper cable needs to be added from the keyboard PCB to the mainboard PCB.

To simplify modification and customization beyond the initial setup, I made these jumper use the footprint of a 9-pin DIP switch.

## Variations

Following are a few potential variations:

(Keyboard with no numpad with custom shield - smaller spacebar)

(Keyboard with additional keys next to the spacebar)

(Keyboard with a "Reset" key in place of "Break")

(Keyboard with light number keycaps similar to the Model 4)

## Project Details

The project consists of multiple parts, each with its own ordering process and consecutive assembly.

The parts are:
- PCB replica - Provides holes for MX style keyswitches and moves ICs and other components to a place that less likely interfers with the shield and keyswitches. Additionally, provides electrical customizability.
- Sheetmetal shield - This is required as the MX style keycaps have a much lower profile, requiring to move the shield closer to the case and keyboard bezel to be accessible. You can't use the original shield used for example for the sculpured ALPS keycaps.
- 3D printed parts (LED standoff and bezels) - Provides optional parts like a much smaller LED standoff and various keyboard bezels to support all variations.
- Custom keycaps - Keycaps with labeling that resemble closely the original keycap style. However, the keycaps are an OEM design and not sculpted like the originals. Each set supplies variations on color to enable customization.

The assembly of the keyboard is described in the [Assembly Guide](TODO).

### PCB

The PCB has been implemented using KiCAD 7. The KiCAD project files are included in this repository.

![E2 Replica Front](/Latest/TRS80_Model_I_Keyboard_MX_E2_3D_Front.png)
![E2 Replica Back](/Latest/TRS80_Model_I_Keyboard_MX_E2_3D_Back.png)

In the "Latest" folder, you'll find the most up-to-date design files, including:

- Gerber files suitable for popular online PCB manufacturers like [PCBWay](/Latest/TRS80_Model_I_Keyboard_MX_E2_Gerber_PCBWay.zip) and [JLCPCB](/Latest/TRS80_Model_I_Keyboard_MX_E2_Gerber_JLCPCB.zip). Most manufacturers should be fine with either.
- A Bill of Materials (BOM) in [PDF](/Latest/TRS80_Model_I_Keyboard_MX_E2_BOM.pdf) format.
- The [full schematics](/Latest/TRS80_Model_I_Keyboard_MX_E2_Schematics.pdf) of the E2 revision.

#### RetroStack Libraries

To work with this KiCAD project, you'll need the RetroStack libraries for KiCAD. Please [follow this link](https://www.github.com/RetroStack/KiCAD-Libraries) to access and install these libraries.

### Keycap Order Instructions

Go to: https://www.maxkeyboard.com/iso-layout-custom-color-cherry-mx-keycap-set-top-print-blank.html
If URL doesn't work anymore, select the ISO layout keycap set for MX to have custom prints on top.

Top Section:
- Select “105” (ISO 105-key (FULL SIZE) +US$5.00)
- Select “6.0” (6.0x Unit Spacebar)
- Select “A” (Top Print +US$15.00)
- Select “NO I have my own” (if you don’t want a keycap puller)
- Select “I will upload my print file (+US$10.00)”
- Upload the file at “Upload Your Artwork” (the .ai file)
- Add a comment “Please do not use homing keys!” (These are the little plastic dots and lines to find “home” without looking; this isn’t on the old keyboards)

This will be about US$55 without tax and shipping (early 2024).

NOTE: Some of the following steps were already defined above or in the file. Not sure what has precedence here, so do both the same just to be sure.

Now, what is left is the overall color design in the “DESCRIPTION” section at the bottom of the page:
- For 1. Bottom Row, select “6.0x Spacebar Row”
- For 2. Keycap Color, select the color “Black” (first) and select “All Keys”. Then, select “beige”(4th) (white is too bright and beige fits better in my opinion), and click on the keys which should be white (I marked them in the preview picture above). Select the most right “Reset” key and click “red”. The template has a few repeated keys each with a different color scheme. This gives you the opportunity later to choose the one which you like the most.
- For 3. Alphanumeric, leave everything as-is
- For 4. Modifiers, leave everything as-is
- For 5. OS Key, leave everything as-is
- For 6. Text Color, click “white” (2nd) and “All Keys”. Then select one white keycap and click “black” (1st), and select all other white keycaps. (Probably not needed, but just in case!)
- Make checkmark at “I confirm that the layout is correct”

Finally, scroll up and click “Add To Cart”.

Then, go to the cart and do the rest.

## Main TRS-80 Model 1 Repository

For additional resources related to the TRS-80 Model 1, be sure to check out the central page for the TRS-80 Model 1 on RetroStack. You can find it [here](https://www.github.com/RetroStack/TRS-80-Model-I).

## Support this Project

RetroStack is passionate about exploring and preserving the legacy of older computer systems. My work involves creating detailed documentation and videos to share the knowledge. I am also dedicated to reviving these classic systems by reimplementing them and offering replacement parts at no cost. If you're keen on supporting this unique project, I invite you to visit my [Patreon page](https://www.patreon.com/RetroStack). Your support would be immensely valuable and greatly appreciated!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
