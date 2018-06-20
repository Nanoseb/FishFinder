# Decoding & Reversing the FishFinder

## Requisites

 * Python (2.7)
 * Gnuradio (v3.7+)

## Example usage

### Extracting packets from a recording:

Generate the python script:

	grcc -d . bits.grc

Run the script and extract valid packets:

    cat example-*.cfile | python -u ./ff_fsk.py | ./sanitize

This expects a 16Msps recording with the FishFinder signal at 2.15MHz offset. These values can be changed in the `.grc`

### Interactively verify demodulation:

Use `bits_gui.grc`:

	gnuradio-companion bits_gui.grc
