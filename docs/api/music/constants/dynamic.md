# Dynamic Constants

Dynamic or volume of notes (also known as MIDI velocity) is represented as in the MIDI specification using integers from 0 (silent) to 127 (loudest). That’s a total of 128 volume settings.

The music library defines the following dynamic constants:

```python
FFF         = 120
FORTISSIMO  = 100
FF          = 100
FORTE       = 85
F           = 85
MEZZO_FORTE = 70
MF          = 70
MEZZO_PIANO = 60
MP          = 60
P           = 50
PIANISSIMO  = 25
PP          = 25
PPP         = 10
SILENT      = 0
```