SCLOrkSynths
======================
 
Collection of SuperCollider SynthDefs (synth definitions) with accompanying Pattern demos.

Anyone is welcome to suggest new SynthDefs for the collection.

Main contributors:

*Bruno Ruviaro* @brunoruviaro - team director; responsible for final review of all code, GUI creation, Quark maintenance, creation of some original SynthDefs

*Josh Mitchell* @joshmit - research assistant; responsible for standardizing coding conventions, rewriting SynthDefs to clarify or improve them, adding new amazing original SynthDefs

*Meha Gupta* @mehagupta - volunteer; initial gathering and upload of SynthDefs from mailing lists and public forums; contribution of additional demos

*Diya Menon* - volunteer; contribution of additional pattern demos

Most SynthDefs have their original author credited in the corresponding scd file. However, we could not identify the author for a few SynthDefs. Please let us know if you know the source of a SynthDef that has no author name, we'll be happy to add it.

## Some conventions

SynthDefs should have the following arguments (default values encouraged but flexible):

* out = 0, to be used in Out.ar(out, ...)
* pan = 0, to be used in Out.ar(out, Pan2.ar(snd, pan))
* freq = 440, for pitched synths
* amp = 0.2, for global amp of synth
* att = 0.01, attack time of the main amplitude envelope
* rel = 1, release time of amplitude envelope
* sus = 1, sustain level (as in a typical ADSR)
* dec = 0.1, decay time (as in typical ADSR)
* gate = 1, if using envelopes like ADSR (not needed if using self terminating envs such as Env.perc)

Miscellaneous:

* Use variables snd for main sound (whatever that is) and env for amplitude env. Variations as needed.
* Use doneAction: 2 to make synth free itself after note is done.
* Avoid specifying durations directly inside SynthDef (other than att and rel) -- patterns will take care of durations.
* Keep any relevant comments about the SynthDef as the header of the file (use block comment)
* Use metadata: inside the SynthDef in the following format, where "category" corresponds to the name of the SCLOrkSynths subfolder where the SynthDef is saved:

```
},
metadata: (
	credit: "name of author(s) of SynthDef",
	category: \drums,
	tags: [\percussion, \kick]
)
).add;
```

# Project description from 2019:

Goal: Create a pool of freely available synth definitions in SuperCollider.

Description: This research project aims to create new open source software synthesizers in the SuperCollider language. The new synthesizers will not only used by SCLOrk (the Santa Clara Laptop Orchestra), but also made available to the computer music community as a Quark. 

## Tasks
* Write original Synth Definitions based on established synthesis techniques;
* Transcribe selected presets from open source software synthesizer such as Helm into SuperCollider language;
* Analyze Synth Definitions by other SuperCollider users and standardize the code to fit our project guidelines;
* Create short, compelling musical sequences using Pbind to demonstrate the potential of each Synth Definition.

## Sources

### SynthDefPool
Link: https://github.com/supercollider-quarks/SynthDefPool
Comment: This is a quark that has not been updated in a few years. We can incorporate all SynthDefs from there. Note how metadata is used.

### sccode
Link: http://sccode.org/ 
Comment: Lots of stuff on here, some of which are SynthDefs that we can incorporate into our collection. Other pieces of code may have interesting sound ideas that we could *convert* into a SynthDef. This is an example of what we can find in sccode: https://sccode.org/1-57g and http://sccode.org/1-522 (three kicks and an FM Rhodes piano by Nathan Ho). Searching by a tag like "instrument" is a good starting point: https://sccode.org/tag/category/instrument 

### synthDEFaults
Link: http://sccode.org/1-5aD 
Comment: This is a compilation of SynthDefs much like what we are trying to do. It's open source, so we can copy, adapt the formatting to our purposes, and share again within our collection with due credit given (metadata in each SynthDef):

### Helm
Link: https://tytel.org/helm/
Comment: this is a cool software synthesizer with a bunch of interesting presets. We can recreate some of these presets by analyzing how they are made and writing equivalent SuperCollider code.




