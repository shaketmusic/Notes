Downward Compression is one of the most important tools we have and use. Compression turns down the loud parts.


### The Parameteres
**Threshold** – anything above the threshold gets turned down. When are we turning down the audio

**Ratio** – by how nuch do we turn the audio. 1:1 ratio is for every 1 dB over the threshold the output will be 1 (no effect)**.** 2:1 for every 2 dB above the threshold the output will be 1dB (compressing in half).

**Attack** – how fast will the volume reduction occur once the audio crossed the threshold.

To get your attack right, slam the compressor (ratio and threshold all the way). Then slowly make your attack slower – now we only hear the attack. When we get the attack we like we make the compressor behave normally (turn up the threshold and turn down the ratio a little bit).

**Attack shapes every rising waveform above the threshold**

**Release** – when the audio gets quite, the compressor needs to disengage. Release is how quickly it resets.

**Release shapes every descending waveform above the threshold**


### Using Compression
We use compression to solve two types of issues - Macro dynamic issues and micro dynamic issues.

### Macro dynamic issues
compressors can help deal with detail that gets lost in the mix.

1. Set your threshold so that it just reaches the quite part a little.
2. Then amplify anything by the average of what you’re attenuating.
3. So it’s about looking for the **quietest part** and compressing the rest, so everything becomes more even.

- Compressors don’t care for frequencies, so it’s good to remove rumble with an EQ before putting a compressor (because it gain we’re not hearing but the compressor is).
- It’s good to use oscilloscopes to see the waveform
- If a human played it, or it was recorded with a mic, it probably needs micro compression


### Micro Dynamic Issues
When the note itself has dynamic problems. Reshaping the internal dynamics.

1. Pull the threshold until we flatten the note. If we want more attack, make the attack slower until you get a good attack.
2. pull the compressor back to a reasonable setting
3. Lift the whole audio by the average of what gets compressed


### Compression Tips
**Peak vs RMS** – affects the threshold. In RMS mode, the threshold looks at the average volume of the audio. Peak mode looks at the instantaneous moment so it’s much more accurate.
RMS is good for Vocals and other legato instruments, while peak is good for drums and hits.

**Glue Compression** – putting a slow attack on a master to make the track feel fatter and more punchy. Good for drums group, synth groups, master

**Drums that knock** - to make drums punchy, put a clipper after a slow attack compressor. So, we add attack and re-flatten the whole thing. This is how splice does kicks.

> Learn how to hear compression first, then worry about the difference between optical and vca compressors.

  

### Multiband Compression - 
Looks like an EQ, acts like a compressor. We set it up to only bring down the specific frequency we want.

A lot of the times, harshness in the highs or boominess in the lows is not about the amount, but of **how long there is the a lot of the frequency**. Multiband compression can solve these problems without losing the body or highs. Isolate the problematic frequencies and compress them, keeping a little of the attack.  You can control kicks that way.

### Side Chain
Sidechain is always on. The audio comes in and gets duplicated to the side chain. The side chain is the analysis portion of the compressor. It controls the gain reduction but we never hear it. We can have either internal (default) or external sidechain.
**The sidechain is always active even when not using an external source**. 

Sometimes when we have a lot of information in the side chain, it’s good to have the unwanted frequencies filtered so that they are not triggering the compression. **Basically whenever we don’t like how the low end makes the compressor sound.**

like when we have a huge kick in a drum loop we filter the low-end out of the side chain so that we can compress better. This is common in mastering compressors.

- It's also good for low notes in vocals: filter the lows on the sidechain.
- Good for some bass performances


A De-Esser is a compressor with a sidechain band pass filter on around 6k. You can make a De-Esser with a regular compressor that way.



### External Side Chain
When we’re using another sound source (like the kick, for example) for the side chain. So instead of listening to the sound we’re compressing it’s listening to the external audio.

- When using the kick for side chaining it’s a good idea to filter out the lows to have more control of the release time.

- You can’t over compress a track with external side chain compression. Because they’re only responding to external audio sources. Don’t be afraid to stack them.

- In ProTools we need to use a mono bus for the external sidechain. Make sure you rename the bus and set it to pre fader.

- You can sidechain to a gate for the opposite effect

> Today most producers use side chain volume controls like Cableguys' Shaperbox or Polyverse's Gatekeeper. There's also a free Max for Live effect called JoyDuck.


---

[[Expanders]]
[[OTT]]
[[Mixing/index|Back]]