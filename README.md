![Alt text](birdie.png?raw=true "Title")

# The 'RAT' Drone Synth

This repository describes my RAT (reverse avalanche transistor) drone synth. I generated the image of the bird using Stable Diffusion (AI).

![](images/lights.jpeg?raw=true)

> [!CAUTION]
> This repository is provided for information only. I am not an electronic or electrical engineer, and so, if you decide to build this project, you do so at your own risk.

## Introduction and inspiration

This project was inspired by the work by [Sam Battle](https://www.lookmumnocomputer.com/bio) of [Look Mum No Computer](https://www.lookmumnocomputer.com/). Sam released a video where he made a synthesiser from a Red Bull can - [watch it here](https://www.youtube.com/watch?v=WjrJeUBjw5g&t=1s). In his related post ['Super simple oscillator'](https://www.lookmumnocomputer.com/simplest-oscillator) he described more of the electronics and a few example schematics. There was also a link to a more technical description of reverse avalanche mode on a blog [BJT In Reverse Avalanche Mode by Kerry D. Wong](http://www.kerrywong.com/2014/03/19/bjt-in-reverse-avalanche-mode/). It was through both Sam's and Kerry's websites that I learned more about the SS9018 and became inspired to make a drone synth.

[This page by 'Pixmusix'](https://core-electronics.com.au/projects/analogue-quad-oscillator-drone-synth/) is perhaps the best I have found so far on this type of oscillator, [its history](https://www.analog.com/media/en/technical-documentation/application-notes/an72f.pdf), how it works and some nice working examples. Pix also provide a very nice animation of this circuit in action. 

## The design

My design is an adapted version of Sam Battle's ['2000 Megadrone Module'](https://www.lookmumnocomputer.com/2000-megadrone). There are schematics and a BOM on his website.

I adapted the design - removed CV, eurorack power and adapted the capacitors to generally be lower in value and therefore lower in pitch.

If you want to build this yourself, you should explore different capacitor values to suit your tastes. I chose 100uF (low), 10uF (mid) and 4.7uF (high). Although if i built another, i might include more variety.

> [!NOTE]
> Vary the capacitors according to your taste. I used 100uF, 10uF and 4.7uF - this is different to the schematic.

The design includes 10 oscillators, each with their own pitch and volume control. Finally, there is a master tone control (a kind of low pass filter). The unit is powered by a 12V DC (2.5mm) male power adaptor.

> [!WARNING]
> I messed up the potentiometer connections and so the pots work in reverse, which is kind of interesting and fits with the whole reverse theme of the synth. Some people may be annoyed or not like this - proceed at your own risk.

I designed the schematic and PCB in [KiCAD](https://www.kicad.org/) - which is incredible and its free! My schematic, PCB and drill templates are included in this repository.

![Schematic](schematic/drone_ting.png?raw=true)

## The PCB

The PCB is simple, 2 sided with pots and LEDs on one side and all other components on the other. I had mine made by [JLCPCB](https://jlcpcb.com/), costing $11.40 + postage - for 5! If you want to order the same for yourself - navigate to the \gerbers\send_to_PCB_manufacturer.zip - simply upload this to your chosen manufacturer to order.

![PCB front](images/pcb_front.jpeg?raw=true)
![PCB front](images/pcb_back.jpeg?raw=true)

This is a very beginner friendly build, all through hole components and nothing too small.

## Bill Of Materials

I used Tayda to source all my components, apart from the 10x SS9018, which i sourced from e-Bay (£7.95 + postage).

- [Fairchild SS9018 VHF RF Bipolar Transistor](https://www.onsemi.com/download/data-sheet/pdf/ss9018-d.pdf)
- [LM386](https://www.taydaelectronics.com/lm386-audio-amplifier-1-channel-mono-class-ab-325mwx1at8-ohm-4v-12v-pdip-8.html)
- [100K OHM Linear Taper Potentiometer Round Shaft PCB 9mm](https://www.taydaelectronics.com/100k-ohm-linear-taper-potentiometer-round-shaft-pcb-9mm.html)
- [10K OHM Linear Taper Potentiometer Round Shaft PCB 9mm](https://www.taydaelectronics.com/10k-ohm-linear-taper-potentiometer-round-shaft-pcb-9mm.html)
- [KN1360 ABS Fluted Black Knob 16x12mm](https://www.taydaelectronics.com/kn1360-knob-black.html) - these are for the volume and tone knobs for each oscillator. I used a slightly larger knob for the master tone.
- [REAN Neutrik NYS229 6.35mm 1/4" Mono Chassis Socket](https://www.taydaelectronics.com/neutrik-6-35mm-1-4-mono-chassis-socket-jack.html)
- [DC Power Jack 2.5mm Panel Mount Round DC-099](https://www.taydaelectronics.com/dc-power-jack-2-5mm-x-5-5-mm-round-type-panel-mount-dc-099.html)
- [5mm Bezel LED Holder Chrome Metal](https://www.taydaelectronics.com/5mm-bezel-led-holder-chrome-metal.html)
- [LED 5mm Red Super Bright](https://www.taydaelectronics.com/led-5mm-red.html)
- Example capacitor: [10uF 50V 105C Radial Electrolytic Capacitor 5x11mm](https://www.taydaelectronics.com/10uf-50v-105c-radial-electrolytic-capacitor-5x11mm.html)
- All resistors: [1/4W 1% metal film](https://www.taydaelectronics.com/resistors/1-4w-metal-film-resistors/test-group-2.html)
- [1N4148 Switching Signal Diode](https://www.taydaelectronics.com/1n4148-switching-signal-diode.html)
- [1 small ceramic disk capacitor](https://www.taydaelectronics.com/capacitors/ceramic-disc-capacitors/test-group-2.html)

## The enclosure

I wanted an 80's industrial submarine type vibe to suit the very heavy and industrial sounds that this drone synth can produce. I opted for a [1590DD Style Aluminum Diecast Enclosure from Tayda](https://www.taydaelectronics.com/1590dd-style-aluminum-diecast-enclosure.html). I also got them to do all the [custom drilling](https://www.taydaelectronics.com/1590dd-custom-drill-enclosure-service.html) on the front. I have included the drilling template in the KiCAD files. Screenshot of this below:

![](images/drill.png?raw=true)


## The finished article

![](images/side.jpeg?raw=true)

![](images/detail.jpeg?raw=true)

![](images/super_close.jpeg?raw=true)

It turned out to be exactly how I imagined. I have contemplated laser etching some labels and things onto the synth front, but I actually like the fact that its clean and blank and is intriguing. It is after all, an incredibly simple instrument to use.

## 'Technical' audio demo

Below is an image of the waveform of one 10uF oscillator. 

![](images/scope.jpeg?raw=true)

I also recorded a video where I connected the synth to my Focusrite Scarlett Solo, passed into Ableton Live and used Pro-Q3 and [jo.Floating Oscilloscope 1.1](https://maxforlive.com/library/device/1918/jo-floating-oscilloscope) - see screenshot below. In the video, I slowly bring in each of the different (4.7uF, 10uF and 100uF oscillators) and change their volume and pitch. Pro-Q3 shows the frequency form of the sound and the oscilloscope (although not ideal) gives some idea of the waveform. The video can be accessed [here on YouTube](https://youtu.be/z13XVZWmLFw).

![](images/youtube.png?raw=true)

## Sound demo

![](https://github.com/cairanvanrooyen/rat_drone_synth/blob/main/demo.wav?raw=true)

## Lessons learned and future ideas

1. Get the pots the right way around ;)
2. Maybe have a cutout section in PCB to allow for power and audio jacks
3. More variety in capacitor values
4. Get Tayda to drill power and audio
5. Maybe laser etch the face
6. More additions: distortion, delay, wavefolder, on/off switches, CV, LFO, switching different caps and more...


