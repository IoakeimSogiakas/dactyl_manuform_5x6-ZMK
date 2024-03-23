****Dactyl Manuform Keyboard. Here is what you need to KNOW****

**Dactyl Manuform keyboards** with **ZMK** (Zephyr-based Microcontroller Keyboard) firmware work by utilizing ZMK to manage keyboard functionality.
**ZMK** is an **open-source firmware** designed for **wireless mechanical keyboards**. It's built on top of the **Zephyr RTOS** (Real-Time Operating System), providing a **flexible** and **reliable** platform for custom keyboard firmware.

To set up a **Dactyl Manuform keyboard** with **ZMK**, you typically start by flashing the **ZMK firmware** onto the microcontroller of your keyboard. 
This firmware enables **wireless connectivity**, **key mapping customization**, and other features. In our case **SPLITS**.

How to do this the simplest way is this: 

**Compiling and flashing**

* Fork this repo by clicking on the Fork button (basically with this you copy this code to your account) it has all the necessary code for you to start.
* Then you go to this website [Keymap Editor](https://nickcoutsos.github.io/keymap-editor){:target="_blank"} (which is from this guy `https://github.com/nickcoutsos/keymap-editor` all props to him for this amazing tool).
* In here you connect your GitHub account and find your repo you can ask me any question that you might have by submitting an Issue.
* When that is done click on save (in the site) this will also save all your changes in your GitHub account.

**We are getting close. Four more steps**

* Go back to your repo (=repository) and go to actions. When it is done (hopefully without any errors if yes again send me an issue for help) download the file it should be a zip file called firmware.zip
**Last step flashing**
* In the zip file you should find two files with the name `dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf2` and `dactyl_manuform_5x6_right-nice_nano_v2-zmk.uf2` this is your firmware
* Now get one of the two halves and get it into bootloader mode. To do this first power it on and then connect it to USB with a computer, then with something like a paper clip press the button next to the USB (between the USB and the on-off switch)
* This should make a new folder in your PC appear called **NICENANO** you then drag the corresponding file into that drive (the nicenano one) and that is it. You did it. (did it for the second half as well)

**Known issues**
* ZMK only reports the battery of the central half the left one.
* If you want to communicate with usb you can definitely do so by connecting the ***LEFT*** half the right one (the peripheral doesn't work like that)
* You can charge by connecting them with a cable. As said above if the cable is connected to the left one it will both charge and also work at the same time without Bluetooth the right one just charges.
* Your Bluetooth needs to be 4.2 at a minimum otherwise it will not work with Bluetooth.

NOTE:
***I would highly advise you to give [ZMK](ZMK.dev){:target="_blank"} a read it literally has everything you would need to know.***
