Digital modes mainly run using AFSK (audio frequency shift keying) and all you need is a computer sound card to get started. It sounds so easy, but getting started was so hard. Here's what I started with:

* Rig: ICOM IC-718

* Antenna: Off center fed longwire, about 124 ft. long up about 35 ft.

* PC: ASUS Laptop

Being a hobbyist, I like the DIY approach. So rather than buying a commercially built interface, I looks for adapters.

### CAT control:

Before I got seriously researching how to homebrew my own digital interface, I thoulght it would be easier to just buy this CAT interface cable.

Cable: Valley Enterprises Icom CT-17 USB FTDI Chipset CI-V Cat Control Programming Cable 3 Feet.
Cost: $29.98 ($25.99 + S&H Amazon)

### AF/PTT: Home Brew.

Interface Cable: MFJ-5213
Cost: $13.95
Pinout:

 Pin | Color | Description
 --- | --- | ---
 1 | Black |
 2 | Brown |  Ground
 3 | Orange | PTT / Transmit
 4 | Yellow |
 5 | Green  |
 6 | Light Green|
 7 | Blue |
 8 | Purple |
 9 | White|
10 | Red |
11 | Pink | Send Audio
12 | Gray | Receive Audio
13 | Light Blue |

Ground Loop Isolation: Psk-31 "EASY DIGI™" Sound Card Interface PSK RTTY SSTV NBEMS JT-65 PCB KIT
Cost: $11.04 ($7.95 + shipping on Ebay)

USB to serial converter: Qunqi 3.3V 5.5V FT232RL FTDI USB to TTL Serial Adapter Module for Arduino Mini Port.
Cost: $7.69 Amazon

I needed to add a transistor and two resistors for an inverter between the DTS output from the USB to serial adapter and the EASY DIGI card opto isolator. I found out that the RTS key was not useful because it only sets 3.3v as voltage high. DTR has 5v as logic high, however, the opto-isolater itself is an inverter. Pin 3 on the accessory Port needs to go from logic high to ground. The opto-isolator does this when activated, but to activate the opto-isolator, it's inout needs to go from low voltage to at least 5v.
