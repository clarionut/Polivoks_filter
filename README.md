# Polivoks_filter
A Eurorack version of the famous Polivoks filter

Here is the original schematic of the filter portion of the Polivoks filter board (the remainder of the board is an envelope generator for modulation of the filter cutoff) -

<img width="652" height="390" alt="image" src="https://github.com/user-attachments/assets/52ffe5a3-95ed-4f81-abdb-9b8128beac22" />

(1: CV input, 2: Audio input, 3: BP out, 4: LP out)
It's a deceptively simple circuit based on two К140УД12 programmable op-amps as the non-linear elements, using their variable slew rate as the basis of the filter. The КР140УД8Б is a simple general-purpose op-amp to mix the control voltages, and the КТ315Г is a general purpose NPN transistor which controls the programming current to the К140УД12 chips. The К140УД12 was a soviet-era copy of the uA776 so I hoped that using an MC1776 (a more modern equivalent) would work OK. Other copies of the filter (e.g. by [Marc Bareille](http://m.bareille.free.fr/modular1/vcf_polivoks/vcf_polivoks.htm)) have used a TL072 in place of the КР140УД8Б and a 2N3904 in place of the КТ315Г. I made these substitutions and found that the circuit worked well on a breadboard.

For use in a modular synth the circuit also needs inputs and outputs (unlike the hard-wired signal paths in the Polivoks). I decided to have two CV inputs, one with an attenuverter (the idea came from Marc Bareille's circuit but the implementation is completely different). The behaviour of the filter is rather dependent on the input signal amplitude so I added a passive attenuator on the audio input. There are separate buffers for the lowpass and bandpass outputs plus an (approximately) equal-power mixer giving a third output continuously variable between LP and BP.

I particularly wanted to give this module a convincing Polivoks style so I decided to label it in white on a black background with Russian legends and graphic elements based on the real Polivoks. The graphics I used are in the Panel folder (Polivoks.svg) but I've also included a version with legends in English (Polivoks_EN.svg).

<img title="Polivox filter" width="200px" src="https://github.com/user-attachments/assets/725bd5b6-9937-4f49-85dc-db482fbee568">

I also 3D printed some Polivoks-inspired (but Eurorack sized) [knobs for the potentiometers](https://www.thingiverse.com/thing:7183551) and am very pleased with the final result.

The sound is very similar to my original Polivoks over most of its range, though the self-oscillation behaviour at extreme resonance settings is slightly wilder than the original.

There are PDFs of the schematic and PCB layout in the Schematics folder along with a copy of the KiCad project. The KiCad project uses some custom symbols, so you may need to download my [custom KiCad libraries](https://github.com/clarionut/kiCad_libraries) and tell KiCad where to find them.

I've also included the Gerbers in case anyone wants to use my PCB layout without any changes.
