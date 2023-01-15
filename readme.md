# SAE J2716 (SENT) decoder for Sigrok
A feature-*in*complete [SAE J2716](https://www.sae.org/standards/content/j2716_201001/) (SENT / Single Edge Nibble Transmission) decoder for [Sigrok](https://sigrok.org/wiki/Main_Page), with support for SPC (Short PWM Code).

![Example image of the decoder in action](/decoder.png?raw=true "SENT decoder with SPC support")

Created as part of my vehicle-hacking project since I can't seem to find good, open-source decoders that could decode SENT signals that also includes SPC pulses.

Note that this project is considered a work-in-progress, and the code is not tested against different types of SENT captures just yet, so it may or may not work for you - use with caution!

Pull requests are welcome for everything from bugfixes to additional features :)

### TODO

* Python object exports to enable stacking of higher level protocol analyzers on top of this thing
* Actually decode SPC pulses, right now the decoder just skips over it
* SENT pause pulse handling (don't have the traces/devices that does this to test yet)
* A more robust method of separating SENT frames rather than just time interval...
* Comprehensive testing of decoder against different SENT traces (especially those without SPC)

### Installing me
On Ubuntu Linux: place (or symlink to) the entire decoder directory in `/usr/share/libsigrokdecode/decoders/`.

### License
MIT - see `license.md` for more details.