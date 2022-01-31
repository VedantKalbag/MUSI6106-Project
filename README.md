# MUSI6106-Project

We are making a JUCE plugin based on the work from the GitHub page GuitarML, specifically “PedalNetRT” (https://github.com/GuitarML/PedalNetRT). This uses PyTorch to train models for guitar amp simulation, but it is written in Python so in order to train new models for your amp simulator, you need to know how to run Python programs and have the whole environment configured correctly and then how to upload the outputted JSON files into the associated amp simulation plugin, SmartGuitarAmp. We will solve this problem of training guitar amp models by rewriting the PedalNetRT Python programs in C++ using the PyTorch C++ API (https://pytorch.org/cppdocs/). Then, our C++ converted PedalNetRT programs can be used in a JUCE GUI plugin similar to the SmartGuitarAmp (https://github.com/GuitarML/SmartGuitarAmp) that will take the output of the models directly into the amp simulation. The plugin will have an intuitive GUI where the user can upload wav files of their desired amp tone, and then save each model as a “preset” on their DAW. If we have time, we will add extra effects into the plugin to create a mini signal chain within one plugin, which may include reverb, EQ, or compression. The code for the JUCE plugin will be heavily based off of the SmartGuitarAmp project, with our adaptation of PedalNetRT built in. 

The plugin is targeted at guitar players who want to record into a DAW with the sound of their ideal amps, and is especially useful for an artist on the go. Once the training recording is done, they never need to record the amp again and can put any variety of amplified guitar directly into their mixes. It is easier to use than other amp simulators, as you either get less choice in tone or too many controls with standard amp simulation plugins. Our plugin gets straight to the tone you want, no fuss.

## Implementation Plan and References
<img width="378" alt="Screen Shot 2022-01-30 at 9 14 24 PM" src="https://user-images.githubusercontent.com/63812135/151730174-92bc3f79-4e5c-4c28-a47e-ff160b491869.png">

- PedalNet - Model Generation
  -  A python real-time guitar model training program - https://github.com/GuitarML/PedalNetRT
  - PedalNet is based on “Real-Time Guitar Amplifier Emulation with Deep Learning” - https://www.mdpi.com/2076-3417/10/3/766/htm
- SmartGuitarAmp - Interface for Sound Recreation
  - A VST Plugin - https://github.com/GuitarML/SmartGuitarAmp

