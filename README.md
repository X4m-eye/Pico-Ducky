# Pico-Ducky
_____       _____      ____      ____                ______       ______                                      ____________       ____           ____       ____________
\    \     /    /     |    |    |    |              /      \     /      \                                    |            |     |    |         |    |     |            |
 \    \   /    /      |    |    |    |             /        \   /        \                                   |     _______|     |    |         |    |     |     _______|
  \    \_/    /       |    |    |    |            /    /\    \_/    /\    \             _______________      |    |              \    \ ______ /    /     |    |
   \         /        |    |____|    |           /    /  \         /  \    \           |               |     |    |_______        \                /      |    |_______
    |       |         |              |          /    /    \       /    \    \          |_______________|     |            |        \____      ____/       |            |
    |       |         |_________     |         /    /      \_____/      \    \                               |     _______|             |    |            |     _______|
   /    _    \                  |    |        /    /                     \    \                              |    |                     |    |            |    |
  /    / \    \                 |    |       /    /                       \    \                             |    |_______              |    |            |    |_______
 /    /   \    \                |    |      /    /                         \    \                            |            |             |    |            |            |
/____/     \____\               |____|     /____/                           \____\                           |____________|             |____|	     	  |____________|




Author          :           X4m-Eye

Description     :           Turn your Pi-Pico/Pi-Pico-W in a Rubber Ducky


This project was not made by me, it was made by dbisu (https://github.com/dbisu/) (https://github.com/dbisu/pico-ducky) 

I am just explaining, what to do in another words and how i did it


How to Create a Pico-Ducky with a Pi-Pico or Pi-Pico-W


To create a Pico-Ducky using a Pi-Pico or Pi-Pico-W, you first need to identify which model you have. If you are unsure, follow these steps:


Identify Your Raspberry Pi Model:

First, determine whether you have a Pi-Pico or a Pi-Pico-W by comparing your board to the images in the following URLs:

this is the Pi-Pico   == https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.electronics-lab.com%2Fwp-content%2Fuploads%2F2021%2F02%2FPICOBOARDWHITEANGLE2-scaled-1.jpg&f=1&nofb=1&ipt=00e4f991c0bee7aeb382f54c3b1bb9604e68e421924a6324445ad9defeae90af&ipo=images

this is the Pi-Pico-W == https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.tiendatec.es%2F8692-large_default%2Fraspberry-pi-pico-w.jpg&f=1&nofb=1&ipt=ae33451481d68e253e3ac4f8aca2bea484eb4e181edbdb924cc9c438e5d3c783&ipo=images

both pictures are in my Github-Project


Boot Your Pi-Pico/Pi-Pico-W:

You have a button on your Pi-Pico or Pi-Pico-W, which is the boot button.

Hold down this button and, while holding it, plug in a micro-USB cable into your Pi-Pico/Pi-Pico-W.

You should see a popup in your file explorer, displaying two files named "INFO_UF2" and "INDEX," and your device should be named as "RPI-RP2."


Nuke-Flash Your Pi-Pico/Pi-Pico-W (if necessary):

If you've previously used your Pi-Pico/Pi-Pico-W and need to erase any data (ensure you've saved any important data), copy the "flash_nuke.uf2" file from my GitHub project to your device.

Your Pi-Pico/Pi-Pico-W should restart. The restart could take a few seconds.


Flash Your Pi-Pico/Pi-Pico-W with the Required Firmware:

Enter boot mode on your Pi-Pico/Pi-Pico-W.

In my GitHub project, you should find two firmware files: "adafruit-circuitpython-raspberry_pi_pico-en_US-8.0.0.uf2" for Pi-Pico and "adafruit-circuitpython-raspberry_pi_pico_w-en_US-8.0.0.uf2" for Pi-Pico-W.

If you have a Pi-Pico, copy and paste the file named "adafruit-circuitpython-raspberry_pi_pico-en_US-8.0.0.uf2," and your Pi-Pico should restart. The restart could take a few seconds.

If you have a Pi-Pico-W, copy and paste the file named "adafruit-circuitpython-raspberry_pi_pico_w-en_US-8.0.0.uf2," and your Pi-Pico-W should restart. The restart could take a few seconds.


Next Steps:

Your Pi-Pico/Pi-Pico-W should now have five files and two folders: "settings.toml," "code.py," "boot_out," ".Trashes," ".metadata_never_index," and the folders "lib" and ".fseventsd."

Copy the "lib" folder from your GitHub project to your Pi-Pico/Pi-Pico-W (replace it if necessary).

Copy the following files from your GitHub project to your Pi-Pico/Pi-Pico-W: "boot.py," "code.py" (replace if you already have one), "duckyinpython.py," "webapp.py," and "wsgiserver.py."


Changing the Keyboard Layout (Optional):

In the "lib" folder, you will find several files. Select the ones corresponding to your language, and delete all others. For example, if you are using German (de), you will need the files named "keyboard_layout_win_de.mpy" and "keycode_win_de.mpy."

Refer to this page for a list of supported languages: https://github.com/Neradoc/Circuitpython_Keyboard_Layouts/releases/tag/20221209

Do not modify the "adafruit_hid" directory, and do not change the file names or extensions; simply choose the correct files for your language.


Locating Your Payload:

Visit the following page: https://github.com/hak5/usbrubberducky-payloads

For example, you can visit this page: https://github.com/hak5/usbrubberducky-payloads/blob/master/payloads/library/prank/NoMoreIcons/payload.txt

On these pages, you will find a .txt file with code that will be your payload.

Open your text editor (e.g., Notepad) and copy the payload code from the website.

Save the file with the extension ".dd" and ensure that you select "All File Types" as the file type.

Copy the newly created ".dd" file to your Pi-Pico/Pi-Pico-W.

I will modify the payload a little bit. I will write more delay into the script. (if you want to use my "payload.dd" go to "My-Pi-Pico" and copy paste the "payload.dd" file)


Disabling Setup Mode:

If you've used your Pi-Pico/Pi-Pico-W, you've likely noticed that it is detected as a USB drive during setup mode.

To disable setup mode, you will need a jumper.

Connect the jumper from pin 18 (GND) to pin 20 (GPIO15). This will prevent the Pico-Ducky from appearing as a USB drive when plugged into the target computer.


Enabling Setup Mode:

To enter setup mode, connect a jumper from pin 1 (GP0) to Pin 3 (GND).

You should now see the setup mode to modify the payload.


My Pi-Pico:

In my Pi-Pico, I have the "lib" folder containing three subfolders: "adafruit_hid," "adafruit_wsgi," and "asyncio."

In the "lib" folder, there are also two files named "adafruit_debouncer.mpy" and "adafruit_ticks.mpy."

I'm using an English layout, and it works well without a specific keyboard layout, but you should choose what works best for your needs.

In my Pi-Pico's main directory, I have the following files: "wsgiserver.py," "webapp.py," "payload.dd," "duckyinpython.py," "code.py," and "boot.py."

Now you're ready to use your Pico-Ducky. Disable setup mode and connect your Pi-Pico/Pi-Pico-W to the target PC. The payload should run within seconds.
