# Wi-BFI (fork)

This fork is used to process data in https://dx.doi.org/10.21227/znfw-vy94. For the original documentation please visit: https://github.com/kfoysalhaque/Wi-BFI

## Modifications

Three modification were mande in the ```main.py``` file:

1. Auto-detection between MU/SU-MIMO networks in 'AC' standard. 'AX' standard only covers SU-MIMO.
2. Timestamps are saved in an output numpy file.
3. PCAPNG files are read entirely without the need to specify the total number of packets to process.

## Wi-BFI Usage

Run the following in a command line:

```
python main.py <'file name'> <'standard'> <'antenna-config'> <'bandwidth'> <'mac address'> <'file to save timestamps'> <'file to save Vmatrices'> <'file to save BFAs'>

```

Example: 

```
python main.py 11ax_SU_4x2_160.pcapng AX 4x2 160 20:c1:9b:fe:4f:ed timestamp_ax_su_4x2_160 V_ax_su_4x2_160  bfa_ax_su_4x2_160

```

Options for these arguments are noted here:

```
<'file name'>: name of the trace

<'standard'>: 'AC' / 'AX'

<'antenna-config'>: '4x2' / '4x1' / '3x3' / '3x2'/ '3x1'

<'bandwidth'>: '160' *(for AX only)* / '80'/ '40' / '20' *(for AX and AC)*

<'mac address'>: MAC address of the Beamformee from which you want to extract the timestamps, BFAs, and Vmatrices.

<'file to save timestamps'>: Name of the file where you want to save the timestamps

<'file to save Vmatrices'>: Name of the file where you want to save the vmatrices

<'file to save BFAs'>: Name of the file where you want to save the BFAs

```


