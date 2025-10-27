# Polivoks_filter
A Eurorack version of the famous Polivoks filter

<img title="Polivox filter" width="150px" src="https://github.com/user-attachments/assets/725bd5b6-9937-4f49-85dc-db482fbee568">

Here is the original schematic of the filter portion of the Polivoks filter board (the remainder of the board is an envelope generator for modulation of the filter cutoff) -

<img width="652" height="390" alt="image" src="https://github.com/user-attachments/assets/52ffe5a3-95ed-4f81-abdb-9b8128beac22" />

It's a deceptively simple circuit using two К140УД12 programmable op-amps as the non-linear elements, using their variable slew rate as the basis of the filter. The КР140УД8Б is a simple general-purpose op-amp to mix the control voltages, and the КТ315Г is a general purpose NPN transistor which controls the programming current to the К140УД12 chips. The К140УД12 was a soviet-era copy of the uA776 so I hoped that using an MC1776 (a more modern equivalent) would work OK. Other copies of the filter (e.g. [Marc Bareille](http://m.bareille.free.fr/modular1/vcf_polivoks/vcf_polivoks.htm))have used a TL072 in place of the КР140УД8Б and a 2N3904 in place of the КТ315Г
