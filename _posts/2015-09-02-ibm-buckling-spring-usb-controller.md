---
layout: post
title: IBM Buckling Spring USB Controller
excerpt: "A drop-in USB keyboard controller (with customizable keymaps) for the IBM Model M keyboard. It even makes Wheelwriter or RJ-45 Model M keyboards work via USB."
tags: [blog, IBM, IBM Model M, IBM Wheelwriter, Soarer's Controller, mechanical keyboards]
modified: 2015-09-02
comments: true
image:
  feature: ltkcI3g.jpg
  credit: BASLQC, Antonizoon (Lawrence Wu)
---

> This article describes a drop-in USB keyboard controller (with customizable keymaps) for the IBM Model M keyboard. It even makes Wheelwriter or RJ-45 Model M keyboards work via USB.

The **IBM Buckling Spring** keyboards (such as the IBM Model M) are widely regarded as timeless classics of computing, and are a stunning example of the _mechanical keyboard_. Technology tends to improve over time, yet keyboards get worse year after year as manufacturers cut corners to make devices thinner.

Buckling Spring keyswitches are equipped with metal springs that snap against a conductive plate, producing a tactile click. They were designed to emulate the feel and sounds of an IBM Selectric typewriter.

Buckling springs were equipped on every IBM PC (AT, XT, PS/2), and is famously used on the [IBM Model M keyboard.](https://en.wikipedia.org/wiki/Model_M_keyboard) That keyboard can still be used to this day with a PS/2 to USB converter.

IBM Terminals and IBM Wheelwriter typewriters also came with buckling spring keyboards. Unfortunately, these keyboards cannot be converted to PS/2 (and thus USB), since they were never meant to be attached to computers in the first place.

At least, until now.

## IBM Buckling Spring USB Keyboard Controller

![USB Controller
Breadboard](http://i.imgur.com/ltkcI3g.jpg)

The BASLQC's IBM USB keyboard controller is a complete replacement for a major Achilles heel of the IBM Model M: _it's ancient, inflexible, and non-customizable controller PCB_, which uses a PS/2 port. 

Our design fulfills the dreams of [The Great Hierophant](http://nerdlypleasures.blogspot.com/), who envisioned that such a board would rectify many of the issues with the IBM Model M keyboard.

This controller makes it possible to add Function shift or macro keys (Volume Up/Dn, Windows key). Or you can even remap the keyboard to AZERTY, Dvorak or Colemak!

We built this by wiring up the Teensy 2.0 to Trio-Mate sockets, and installing Soarer's Controller. (not to be confused with his AT/XT pin Converter: ours is a lot more advanced.) [More specifications here.](https://github.com/BASLQC/ibm-wheelwriter-usb-controller/wiki)

It's time to bring your IBM Model M into the modern age. Ditch that PS/2 adapter, and plug in a fresh new USB controller to give it another decade. 

[Follow the instructions at our Git repository](https://github.com/BASLQC/ibm-wheelwriter-usb-controller/wiki) to build a controller for yourself. 

Don't worry if you're not as electrically minded: we are planning to _mass produce these keyboard controllers_ as integrated PCBs. Hopefully we will manage to bring the price to $29.99.

### Other Keyboards

In addition, this controller can also be used to make other IBM Buckling Spring keyboards work via USB:

* **IBM Wheelwriter** Typewriter Keyboards (3/5/6, 15, 1000, 1500) - I was inspired to create this keyboard controller when I discovered a broken IBM Wheelwriter typewriter (More on that story below). The Wheelwriter keyboard is actually superior to the Model M, thanks to it's ability for NKRO: 10+ simultaneous key presses. Now you too can rescue these 60% keyboards and use them on modern computers.
* **RJ-45 IBM Model M**, **RJ-45 Model F**, basically any IBM keyboard that uses ribbon cables.

### Features

What makes this keyboard controller so special? Why would you want it on your IBM Model M? Here's why.

* **USB Plug** - No more PS/2 conversion, no more latency, no more power sucking controller, no more wonky PS/2 adapter plugs. It's just pure low-power USB HID. It will even work on Android with a USB Host adapter.
  * **Revive Wheelwriter (Typewriter) and Terminal Model M Keyboards** - Using this controller, you can make Terminal RJ-45 Model M keyboards or even IBM Wheelwriter typewriter keyboards work via USB. We've got keymaps for them all.
* **Replaces Broken or Lost Cables** - If you've ever lost or damaged the coiled PS/2 cable on your Model M, the keyboard becomes effectively unusable, since the keyboard controller uses a proprietary AMP socket. Our new controller allows you to revive that keyboard once again.
* **Fully Customizable Keymap** - Now you can have Function shifted Volume keys on your Model M, get a Windows key (if you want it) or set up macro keys. Whatever you want.
  * **Alternative Layouts** at the Controller Level - You can set the layout to always be Dvorak or Colemak, or whatever custom layout as you prefer. No more OS level configuration.
* **Future Proofing** - The ancient keyboard controller on the Model M is it's only Achilles heel. It sends output through a proprietary AMP socket, which is adapted to PS/2 using a proprietary cable. You need to use a special PS/2 to USB converter that can deal with the high power usage of the ancient controller. The buckling springs have a virtually indefinite lifetime, but this ancient electronic PCB will give out sooner or later. 
  * We can do better. USB is the modern standard for keyboard input, and will remain so for the near future (USB 3.1 Type-C sockets will just need a basic adapter). It's possible to upgrade this controller to work as a Bluetooth HID as well. Your IBM Model M will last for generations to come.