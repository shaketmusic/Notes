**Generators** – Make sound. Each generator method is capable of different types of sounds, so the sound we have in mind decides which sound generation method we use.

- Oscillator (subtractive/wavetable)
- Noise
- Sampler
- Additive
- Physical Modeling
- FM/Phase Modulation
- AM

**Processors** – Processes the sound, changes it.

- Filter
- Distortion
- Amp, Flanger, Delay, Reverb

**Modulators** – change the sound over time. Modulation is the most important part of the sound. It makes the sound feel alive and moving like an acoustic instrument.

- **LFO**
- **Noise**
- **Envelopes**

---
## Basic Oscillator Concepts

### **Unison**
Multiple voices that are slightly different in pitch, and timing. It’s a concept borrowed from choirs and orchestras. Unison sounds huge, wide and lush. No unison sounds focused and clear.

**Fork in the road moment -** A lot of time you need to decide first if you want the sound to be unison or not.

- You can use unison for a riser to make it less clear

- Why not modulate the unison amount? Like with a fast envelope on the detune amount

- Unison with odd number of voice will have a center voice, that’s something to consider.

- Make sure you’re voices’ phases are aligned (or not) the way you want them. You can control this by not making your oscillators free running. In serum you can turn random phase to 0.

- Try to do unison with phase locked. Sounds close to a comb delay.

---
### **Reese Bass**
You can find them anywhere, in any genre. **It’s made of Multiple oscillators (today we use unison) of a harmonic rich wave, filtered.** Was created by Kevin Saunderson a.k.a Reese which was one of the Bellville three, who are considered the fathers of Techno. It was made for the track **Just Want Another Chance**. 

In the song Terrorist, Renegade sampled the Reese Bass and added a break for Amen Brothers, and birthed a whole new genre – Jungle (and after that Drum and Bass).

The problem with Reese Bass is the phase relations that are uneven. To combat that, producers put a single sine wave sub that will give the fundamental. Then they remove the fundamental of the unison saw waves.

![[ReeseBassWave.png|357]]

![[ReeseBassOscillatorConfig.png|362]]

- You can add movement to the Reese bass by modulating the detune amount, add and move a notch filter, chorus, flanger, phaser, distortion

- Because the Reese Bass was originally sampled, its more characteristic to make one note and sample it. Looping also helps the sound be more authentic. Then you can process it with Multiband Compression/Saturation etc.

---

### Neuro Bass

Could be considered an evolution of the Reese Bass, and is present in Neuro-Funk and Drum and Bass. Producers of Neuro Bass created their sounds using what is called **"Mudpie"**. It is a pool of sound material producers scrub through and automate during the drop.

**How to create a Mudpie**
1. Taking a Low sine wave (10-30 seconds long) and putting it through a notch filter, and adding a little bit of drive.
2. Putting Glue Compressor, turning soft clip and turning the makeup.
3. We use the notch filter as a volume by drawing automation curves for the cuttof.
4.  Put a utility with -6 gain. Bounce, Repeat 1-4, Bounce again.
5. Put the bounced audio through Ableton’s Amp Bass.
6. Add Multiband Dynamics to turn up the high with upward compression. Compress the mids and the lows a bit.
7. Put another Notch filter with automation. Bounce
8. Put overdrive and modulate the bandwidth and frequency. Clip again, Bounce.
9. Optional: Put Ableton’s delay to fade mode, put on a very short time and upp the feedback. Modulate the delay time. Bounce.
10. Mix with Modulated filter, saturation on the high, EQ, Multiband dynamic.

![[TheMudPieProcess.png]]

The Mudpie should be edited, not to sound good as it is. We take the best parts, automate them, and arrange them in a musical way.

**Quick tip** -
You can also take a small snippet and drug it into Serum to create a new wavetable. If the wavetable is phasing, you can **set phases this frame to all** under **process all** in the advanced editing. Also do **normalize each to gain separately.** Maybe use the wavetable to FM the second oscillator?

