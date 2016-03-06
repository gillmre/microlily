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

...
```

(For examples look at the test directory)

Yes, as far as documentation goes this README kinda sucks. Pull requests are welcome!

### Available commands

`\athenian` - support for just intonation with Athenian EDA accidentals.

`\he` - Extended Helmholtz-Ellis JI Pitch Notation support.

`\ji12` - just intonation written as 12 note equal temperament (this makes sense when used with cents).

`\promethean` - more precise accidentals than Athenian.

`\regular` - JI retuning, used by the Athenian and Promethean implementations.

`\sagji` - common code for Sagittal with just intonation.

`\sag60` - ratios mapped to 60-equal.

`\sag72` - ratios mapped to 72-equal.

`\sagji224` - Athenian accidentals but consistently applied according to 224-equal.

`\sagji60` - just intonation with accidentals for 60-equal.

`\sagji72` - just intonation with accidentals for 72-equal.

`\trojan` - common code for Trojan notations of JI.

`\trojan60` - just intonation rounded off to 60-EDO.

`\trojan72` - just intonation rounded off to 72-EDO.


### Examples

- [ratios.ly]() - example of JI duplicating the Sagittal paper.
- [harmonics.ly]() - the harmonic series in Extended Helmholtz-Ellis Pitch Notation.
- [subharmonics.ly]() - another Extended Helmholtz-Ellis Pitch Notation example matching one of the defining papers.
- [fig6.ly]() - another Sagittal example.

### Utilities

[addmts.py](), [addmts.py3]() - Retune output MIDI files to use the MIDI Tuning Standard.

