# microlily: Microtonal support for Lilypond

Original code by Graham Breed at https://bitbucket.org/x31eq/microlily.

This package adds support for microtonal notation in Lilypond, including Sagittal and Extended Helmholtz-Ellis notations.

The Sagittal font and musical examples were provided by Dave Keenan and George Secor. There's some kind of license on them.

The HE font for Extended Helmholtz-Ellis Pitch Notation is shareware by [Marc Sabat](http://www.marcsabat.com/) and can be download [here](http://www.marcsabat.com/pdfs/HE-font-2011.zip). The HE font should be installed as a system font.

This package includes the Sagittal font. More information at http://sagittal.org.



## Installation

Install using [lyp](https://github.com/noteflakes.lyp)

```bash
lyp install microlily
```

## Usage

```lilypond
\require "microlily"


```

(For actual examples look at the [test](https://github.com/noteflakes/lyp-microlily/tree/master/test) directory)

(Yes, as far as documentation goes this README kinda sucks. Pull requests are welcome!)

### Available commands

`\athenian` - support for just intonation with Athenian EDA accidentals.

`\he` - Extended Helmholtz-Ellis JI Pitch Notation support.

`\"ji12"` - just intonation written as 12 note equal temperament (this makes sense when used with cents).

`\promethean` - more precise accidentals than Athenian.

`\regular` - JI retuning, used by the Athenian and Promethean implementations.

`\sagji` - common code for Sagittal with just intonation.

`\"sag60"` - ratios mapped to 60-equal.

`\"sag72"` - ratios mapped to 72-equal.

`\"sagji224"` - Athenian accidentals but consistently applied according to 224-equal.

`\"sagji60"` - just intonation with accidentals for 60-equal.

`\"sagji72"` - just intonation with accidentals for 72-equal.

`\trojan` - common code for Trojan notations of JI.

`\"trojan60"` - just intonation rounded off to 60-EDO.

`\"trojan72"` - just intonation rounded off to 72-EDO.

**Note**: as the original code is not very DRY-ish, not namespaced nor modularized, I took the approach of defining commands for loading each of the original files. This way the original functionality is maintained with a minimum of fuss. If anybody feels like improving the API, please do so! - Sharon Rosner

### Examples

- [fig6.ly](https://github.com/noteflakes/lyp-microlily/blob/master/test/fig6.ly) - another Sagittal example.
- [harmonics.ly](https://github.com/noteflakes/lyp-microlily/blob/master/test/harmonics.ly) - the harmonic series in Extended Helmholtz-Ellis Pitch Notation.
- [ratios.ly](https://github.com/noteflakes/lyp-microlily/blob/master/test/ratios.ly) - example of JI duplicating the Sagittal paper.
- [subharmonics.ly](https://github.com/noteflakes/lyp-microlily/blob/master/test/subharmonics.ly) - another Extended Helmholtz-Ellis Pitch Notation example matching one of the defining papers.

### Utilities

[addmts.py](https://github.com/noteflakes/lyp-microlily/blob/master/etc/addmts.py), [addmts.py3](https://github.com/noteflakes/lyp-microlily/blob/master/etc/addmts.py3) - Retune output MIDI files to use the MIDI Tuning Standard.

