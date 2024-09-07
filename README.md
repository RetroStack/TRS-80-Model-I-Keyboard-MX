# TRS-80 Model 1 - MX Keyboard

This project is a reimplementation of the iconic TRS-80 Model 1 computer's original keyboard. My revision replicates the functionality of the original using modern "OEM" MX-style keycaps. The entire project is available under the MIT license.

![E2 Replica](/Latest/TRS80_Model_I_Keyboard_MX_E2_Photo.png)

## Project Details

The project consists of multiple parts, each with its source files, an example ordering process, and consecutive assembly.

The parts are:
- [PCB](https://github.com/RetroStack/trs-80-model-i-keyboard-mx/blob/main/README.md#pcb)
- [Keycaps](https://github.com/RetroStack/trs-80-model-i-keyboard-mx/blob/main/README.md#keycaps)
- [Shield](https://github.com/RetroStack/trs-80-model-i-keyboard-mx/blob/main/README.md#shield)
- [3D printed parts (LED standoff and optional bezels)](https://github.com/RetroStack/trs-80-model-i-keyboard-mx/blob/main/README.md#3d-printed-parts)

Below is a description of the [keyboard customization](https://github.com/RetroStack/trs-80-model-i-keyboard-mx/blob/main/README.md#customizability).

The Assembly Guide is coming soon.

If you like this project, please consider [supporting it](https://github.com/RetroStack/trs-80-model-i-keyboard-mx/blob/main/README.md#support-this-project).

## PCB

The PCB has been implemented using KiCAD 7. The KiCAD project files are included in this repository.

![E2 Replica Front](/Latest/TRS80_Model_I_Keyboard_MX_E2_3D_Front.png)
![E2 Replica Back](/Latest/TRS80_Model_I_Keyboard_MX_E2_3D_Back.png)

In the "Latest" folder, you'll find the most up-to-date design files, including:

- Gerber files suitable for popular online PCB manufacturers like [PCBWay](/Latest/TRS80_Model_I_Keyboard_MX_E2_Gerber_PCBWay.zip) and [JLCPCB](/Latest/TRS80_Model_I_Keyboard_MX_E2_Gerber_JLCPCB.zip). Most manufacturers should be fine with either.
- A Bill of Materials (BOM) in [PDF](/Latest/TRS80_Model_I_Keyboard_MX_E2_BOM.pdf) format.
- The [full schematics](/Latest/TRS80_Model_I_Keyboard_MX_E2_Schematics.pdf)

### RetroStack Libraries

To work with this KiCAD project, you'll need the RetroStack libraries for KiCAD. Please [follow this link](https://www.github.com/RetroStack/KiCAD-Libraries) to access and install these libraries.

### Supported Key Switches

This PCB supports both PCB-mounted and plate-mounted MX-style key switches.

![Supported Key Switches](/Images/Various_Switches.png)

Provided holes cover both footprints on the PCB.

![Footprint Holes in PCB](/Images/Keyswitch_Footprint.png) 

## Keycaps

A template of keycaps is provided that closely resembles the original keycap design.

![Template preview](/Images/Template_Preview.png)

In the "Latest" folder, you'll find the most up-to-date design files, including:

- Keycap template in [Illustrator (.ai) format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Keycap_Template.ai)
- Keycap template in [SVG format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Keycap_Template.svg)

These templates should work with most keycap manufacturers.

### Order Instructions - MaxKeyboard.com

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

The last comment is optional but ensures that you do not have "bumps" on specific keys (e.g., the "F" and "J" key of a modern standard keyboard), which were not on the original keyboard.

NOTE: Some steps were already defined in the template file, but the website is not clear if it needs to be redefined. Just to be safe, follow the next steps as well.

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

It is correct that you can't see the labeling in this preview. That is provided in the template above and will not be applied to the preview you see. Some empty keys won't be used and can be discarded. They do not fit the Model 1 keyboard.

Finally, scroll up and click “Add To Cart”.

You can customize the keycap colors, but be aware that the text color is sometimes white and other times black. Here is a preview with label color for reference:

![Keycap Selection](/Images/Keyboard_Preview.png)

## Shield

![Shield](/Images/Shield.png)

The shield is different from the original keyboard shield as it has to accommodate the much smaller height of the MX key switches. A direct comparison to the original keyboard makes this visible:

![Keyboard Comparison](/Images/Keyboard_Comparison.png)

That also required moving most components to the back of the PCB.

![Moved Components](/Images/Components_on_the_back.png)

In the "Latest" folder, you'll find the most up-to-date design files, including:

- Shield Design in [STEP format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Shield.step)
- [Flat Pattern](/Images/Shield_Flat_Pattern.png) of sheet metal design

The STEP file is accepted by most online manufacturers like [Fabworks](https://www.fabworks.com), [SendCutSend](https://sendcutsend.com), [OSHCut](https://www.oshcut.com/), or [PCBWay](https://www.pcbway.com).

The design uses the following properties which are sometimes required for the ordering process:

- Suggested Material: Steel G90 (SendCutSend), Steel 1008 (Fabworks)
- Thickness: 1.22mm (0.048")
- K Factor: 0.46
- Bend Radius: 0.762
- Finish: Matte Black

### Order Instructions - [Fabworks](https://www.fabworks.com)

Go to [Fabworks](https://www.fabworks.com) and drop the [STEP file](/Latest/TRS80_Model_I_Keyboard_MX_E2_Shield.step) into the upload section (or select it by clicking it).

This will open up a new page and show a small preview of the shield. 

- Select the material "Steel 1008".
- Set thickness to 0.048" or 1.22mm.
- Select "Matte Black" as finish.
- (optionally) Modify the quantity

Click on "Checkout".

NOTE: The original shield has a thickness of 1.5mm. However, if you select 1.5mm and the paint of the finish is added, the thickness will increase, and the key switches won't fit anymore (or at least will not click in). Additionally, the design is for 1.22mm. Changing the thickness to another value will change the position of the mounting holes slightly. Small variations, however, should not be problematic.

## 3D Printed Parts

In the "Latest" folder, you'll find the most up-to-date design files, including:

- LED Standoff in [STL format](/Latest/TRS80_Model_I_Keyboard_MX_E2_LED_StandOff.stl)
- Bezel with Numpad in [STL format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Bezel_with_NumPad.stl)
- Bezel without Numpad in [STL format](/Latest/TRS80_Model_I_Keyboard_MX_E2_Bezel.stl)

### LED Standoff

![LED Standoff](/Images/Keyboard_LED_Standoff.png)

The LED standoff needed to be redesigned from the original since the PCB is much closer to the shield, requiring a reduction in size.

![LED Standoff Comparison](/Images/LED_Standoff_Comparison.png)

This is an optional item and not necessarily required. However, without it, you might struggle to solder the LED to the correct distance to surface the bezel:

![LED Surfacing](/Images/LED_Surfacing.png)

Additionally, without the standoff, you might bump into the LED as it extends above the PCB, and this will hinder you from aligning the bezel and case over the keyboard until you bend it to the right position again.

### Bezels

I've also provided two additional bezels in addition to the [original](https://github.com/RetroStack/TRS-80-Model-I-Parts/tree/main/Keyboard_Bezel) to help cover the two keys in case you do not want to add them.

![Custom Bezels](/Images/Custom_Bezels.png)

An example can be seen here:

![Bezel Example](/Latest/TRS80_Model_I_Keyboard_MX_E2_Photo.png)

### Order Instruction - [JLC3DP](https://www.jlcpcb.com) (service of JLCPCB)

You can print them yourself, but most likely you do not have such a large printer. You can order them online. What follows are instructions for JLC3DP, which I've had good experiences with. Additionally, they take care of sanding and finishing.

- Go to [JLC3DP](https://www.jlcpcb.com).
- Click the "Quote Now" button under the "3D Printing" image.
- Click the "Add 3D file" and select the STL file provided above.

A few options appear. In either case, I always selected "SLA(Resin)" for the technology, which has a very smooth surface.

You can leave "LEDO 6060 Resin" for the LED standoff. That resin is white, and the standoff is hidden anyway inside the keyboard. It is also the cheapest option.
For the bezel, however, I would choose the "Black Resin" option. It is a bit more expensive, but it will reduce post-processing for you as you probably do not want a white bezel.

Leave all other options as-is.

You still have to select a "Product Description". Apparently, this is some customs requirement. I've selected for both "Office Appliances and Accessories" and "Keyboard Enclosure".

You can then hit "Save to Cart" and checkout.

By default, they will review your designs and send you an email to pay within a few hours. Simply go back to your order page (after you've created an account) and select "Pay".

NOTE: Most of the time, however, they will also send you an email to confirm that you want to assume the risk of ordering the design as-is as they are too long and may deform during production or have parts which are too thin. I've always accepted the risk and never had any trouble.

## Customizability

Since there was an opportunity to improve upon the keyboard, I provided various ways to optionally customize your keyboard.

### Additional Keys

Modern keyboards generally use 6 units (6u) wide spacebars (or similar short sizes) instead of the 8 units (8u) the original Model I keyboard used. This replacement keyboard comes with a 6 units wide spacebar, which means that there is additional space next to the spacebar for two additional keys to fill the gap of the original keyboard bezel.

![Full Keyboard with additional keys](/Images/Variations/Full_Keyboard_Additional_Keys.png)

Any key can be [mapped](/Images/Keyboard_Mapper.png) to these two additional keys by selecting the row and column:

![Keyboard Mapper](/Images/Keyboard_Mapper_Small.png)

On the underside, you can add DIP switches (or simply use jumpers) to select the row and column:

![Custom Mapping](/Images/Custom_Mapping_Additional_Keys.png)

NOTE: Make sure to only select one per DIP-switch row. If you select more than one, the keyboard will behave erratically. However, it will also not break anything.

### Remap other Keys

You can also remap the BREAK and CLEAR keys to anything you want:

![Custom Clear and Break](/Images/Key_Mapping_Break_Clear.png)

### Add Reset Key

To emulate a popular Model 3 & 4 keyboard feature, the ability to add a reset key is provided:

![Reset Key](/Images/Variations/Full_Keyboard_Reset_Key.png)

Simply add a jumper to the keyboard:

![Keyboard Jumper](/Images/Keyboard_Reset_Jumper.png)

Then, connect to a via close to the reset circuity on the main board:

![Mainboard Jumper](/Images/Main_PCB_Reset_Jumper.png)

![Connected Keyboard](/Images/Connected_Reset_Jumper.png)

On the back of the board, select Row 9 and Column 9 as shown in the [mapper](/Images/Keyboard_Mapper.png):

![Keyboard Mapper](/Images/Keyboard_Mapper_Small.png)


### Keycap Variations

As each keycap set consists of 105 keys. The basic keyboard without a numpad requires only 53 keys, while with a numpad, it needs 65 keys. Even with the additional 2 keys, we need at most 67 keys. There are 38 keys left (minus some unused key sizes and shapes), which can be duplicated. I've provided a few variations of keycaps in different colors, but also custom prints (like the CTRL key for "Electric Pencil"):

![Keycap Selection](/Images/Keyboard_Preview.png)

This provides a couple of variations (and more):

![Keyboard with additional keys](/Images/Variations/Full_Keyboard_Additional_Light_Keys.png)
![Keyboard with additional keys](/Images/Variations/Full_Keyboard_Light_Numbers.png)
![Keyboard with additional keys](/Images/Variations/Full_Keyboard_Red_Break.png)
![Keyboard with additional keys](/Images/Variations/Keyboard_Light_Keys.png)

## Assembly Guide

1. **Solder Components on PCB**
* Begin by soldering all components on the back side of the PCB. This includes:
  * **Integrated Circuits (ICs)**
    * Match notch on PCB with notch on IC
    * Z1 & Z2 are the 74LS05s, while Z3 & Z4 are the 74LS368s
  * **Capacitors**
    * Both are the same. No orientation needed.
  * **LED resistor**
  * **Resistor network**
    * Match dot on the side of the resistor network with the square on one end of the footprint on the PCB.
  * **Right-angle header**
    * Solder this outward from the keyboard PCB
* Ensure all components are securely soldered and correctly oriented.
2. (Optional) **Install DIP Switches**
  * DIP Switches for additional keys:
    * There are four DIP switches located near the spacebar at the bottom of the PCB. These switches are for configuring the two additional keys next to the spacebar.
    * This step is optional and only necessary if you intend to use these additional keys.
    * Alternatively, you can use jumper cables instead of the DIP switches to set a fixed configuration.
  * DIP Switches for key remapping:
    * Four more DIP switches are located near the CLEAR and BREAK keys at the top right (from the back) of the PCB. These are used to remap these keys.
    * By default, these keys are set to their original mapping. To change the mapping, you need to cut the jumpers next to the DIP switches.
    * This is also optional and not required for standard use.
3. **Solder the LED**
  * On the front side of the PCB, solder the LED into place.
  * Use the stand-off provided to ensure proper clearance from PCB and to align it with the case later on. Align the flat edge of the stand-off with the LED and the graphic on the PCB.
  * Install the LED before adding the shield, as it will be difficult to place the stand-off after the shield is attached.
4. **Install Keyswitches in Corners**
  * Begin by adding keyswitches to all four corners of the keyboard (do not install the spacebar keyswitches yet).
  * Ensure keyswitches are installed in the correct orientation. Note that some keyswitches, such as those for SHIFT keys, need to be oriented differently.
  * Additionally, place a central keyswitch at the H position for extra support. If you are installing a numpad, add keyswitches to all four corners of the numpad.
  * Verify that all pins of the keyswitches are straight to facilitate proper alignment in the next steps.
5. **Align and Solder Keyswitches to Shield**
  * Place the shield with the keyswitches lying flat on a table, with the bottom of the shield facing you.
  * Carefully align the PCB with the keyswitches and lay it flat into the back of the shield.
  * Ensure all keyswitch pins are properly extending out of the PCB.
  * Once alignment is confirmed, solder the keyswitches in place.
6. **Install Remaining Keyswitches**
  * Flip the shield with the attached PCB and proceed to install the remaining keyswitches.
  * For each keyswitch, ensure that the pins are straight and insert the keyswitch vertically into the shield. Push down to lock it into place.
  * Continue this process for all keyswitches, except the spacebar. Remember that some keyswitches may require a different orientation.
7. **Solder All Keyswitches**
  * With all keyswitches in place (except the spacebar), solder them onto the PCB.
8. **Install Spacebar Keyswitches**
  * Install the keyswitches for the spacebar but keep them unsoldered for now.
  * Typically, two outer keyswitches are sufficient. Adding a center keyswitch increases resistance and might affect the feel, so this is a matter of personal preference.
  * The PCB has elongated footprints for the outer spacebar keyswitches to accommodate various spacebar styles.
  * Clip the spacebar keycap (from the keycaps box) into the outer keyswitches (and center if used). Adjust the outer keyswitches if needed to ensure a proper fit.
9. **Test and Adjust Spacebar**
  * Test the spacebar keycap. Check if it presses smoothly or gets stuck.
  * If the spacebar is resisting or sticking, adjust the position of the outer keyswitches until the spacebar moves freely. Usually moving them outward helps.
10. **Solder Spacebar Keyswitches**
  * With the spacebar keycap still attached, flip the keyboard and solder the spacebar keyswitches in place.
  * Keeping the keycap attached ensures that the keyswitches do not shift before soldering.
11. **Add Keycaps**
  * Install all the keycaps onto the keyswitches.
  * The keycap set comes with various color schemes for specific keys. For an authentic look, use white keycaps for ENTER keys and black for all other keys.
  * You can always change the keycaps later if desired.
12. (Optional) **Adjust Metal Shield**
  * Some metal shields may not fit perfectly because they aren’t always bent exactly 90 degrees. Often, they are slightly too wide, making it difficult to fit them into the case without putting excessive strain on the posts.
  * To adjust the fit, hold the assembled keyboard in front of you, angled downward against your body. The metal tabs with the mounting holes should be positioned on the left and right sides of you.
  * Gently press the two metal tabs at the front and back of the shield together, slightly bending them inwards.
    * Apply even pressure on both sides to avoid bending one side more than the other. Uneven bending will prevent the keyboard from fitting properly into the case.
    * __Don’t overbend__ the shield, as this is much harder to correct afterward.
  * Repeat this process for each horizontal section where the holes are located (2 sections in total).
  * After each adjustment, check how the shield fits in the case. It should gradually get closer to the perfect fit with each adjustment.

## User Guide

### Installation

If your old keyboard already uses a header, simply disconnect the old ribbon cable from the computer and/or keyboard, remove the old keyboard from the case, and attach the new cable to the mainboard. I prefer using a 40-pin IDC cable which can be quite short. Ensure that the red side of the IDC ribbon cable faces pin 1 or 2 on both the keyboard and mainboard. Since the IDC cable has two rows per connector, use only one side of the connector—typically the row closest to the notch.

![Attached IDC Cable 1](/Docs/Guide1.png)
![Attached IDC Cable 2](/Docs/Guide2.png)

If you use the wrong row, nothing will break, and the keyboard will simply not work. A good way to check if the connection was made correctly is that the LED lights up when the computer is turned on.

![Connected IDC Cable](/Docs/Guide3.png)
![LED turns on](/Docs/Guide4.png)

### Key Mapping

This replacement keyboard includes optional DIP switches on the bottom, allowing you to reconfigure the additional keys next to the spacebar, as well as the BREAK and CLEAR keys. By default, the BREAK and CLEAR keys are mapped to their original functionality and working as expected. You can remap these keys and the additional keys next to the spacebar using the [MX Keyboard Mapper page](/Latest/TRS80_Model_I_Keyboard_MX_E2_Mapper.pdf) in the Latest directory, which includes a full overview of the M1 keyboard matrix.

**Example**: To remap a key to "T," set the **R**(ow) DIP switch to 3 (R3) and the **C**(olumn) DIP switch to 5 (C5).

**NOTE**: Never switch more than one DIP switch per DIP switch row, as it will result in unexpected key mappings across the keyboard, affecting keys that are completely unrelated due to the matrix. If your keyboard reacts erratically, check to ensure you haven't inadvertently switched more than one key in each DIP switch row.

![DIP Switches](/Docs/Guide5.png)

### Installing the Right-Angle Header on the Mainboard

If your mainboard still uses the foil-type connector, it needs to be removed, as these are prone to failure. The included right-angle header should be installed in its place. 

#### To remove the foil-type ribbon cable

Cut the ribbon cable close to the mainboard. On the small piece left on the mainboard, make a cut between each wire to separate them. This simplifies the removal of each individual wire, reducing strain on neighboring pads and minimizing the risk of lifting pads off the board. After removing all wires, use a solder wick to clean the pads, being careful not to overheat them. Once the pads are clean, solder the right-angle header inwards, ensuring it fits within the case.

![Header](/Docs/Guide6.png)

### Installing the RESET Key

![Solder point on mainboard](/Docs/Guide7.png)
![Connector on keyboard](/Docs/Guide8.png)

To enable the RESET function, connect the jumper wire between the keyboard and the mainboard. Use a Dupont-style wire with a female connector on one side for easy detachment later on. You don't want to solder the mainboard and keyboard permanently together. Solder one end to the marked via on the mainboard and connect the other end to a 1-pin header on the keyboard's RST pad.
To configure the mapping, set the key to **R**(ow) 9 (R9) and **C**(olumn) 9 (C9), and replace the keycap with the red RESET key. This setup allows the keyboard’s RESET key to function as the mainboard's reset button.

![Reset Keycap](/Docs/Guide9.png)

## Main TRS-80 Model 1 Repository

For additional resources related to the TRS-80 Model 1, be sure to check out the central page for the TRS-80 Model 1 on RetroStack. You can find it [here](https://www.github.com/RetroStack/TRS-80-Model-I).

## Support this Project

RetroStack is passionate about exploring and preserving the legacy of older computer systems. My work involves creating detailed documentation and videos to share the knowledge. I am also dedicated to reviving these classic systems by reimplementing them and offering replacement parts at no cost. If you're keen on supporting this unique project, I invite you to visit my [Patreon page](https://www.patreon.com/RetroStack). Your support would be immensely valuable and greatly appreciated!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
