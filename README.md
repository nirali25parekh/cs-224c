# Reproduction of the [Blind Charging Paper](https://5harad.com/papers/blind-charging.pdf)

## Course Project : Stanford CS 224C
- Nirali Parekh

## Basic Usage

The simplest usage of the blind charging algorithm looks like this:
```py
import blind_charging as bc

# Configure BlindCharging to use your locale.
bc.set_locale("Suffix County")

# Run the redaction algorithm passing in:
#   1) The input police narrative text;
#   2) A list of civilian (non-peace-officer) names referenced in the narrative;
#   3) A list of names of peace officers referenced in the narrative.
#
# This returns the redacted input narrative.
civilians = ["Sally Smith"]
officers = ["Sgt. John Jones"]
narrative = "Sgt. John Jones arrested Sally Smith (S1) in Parkside."
bc.redact(narrative, civilians, officers)
# '<Sergeant #1> arrested <(S1)> in <[neighborhood]>.'
```


