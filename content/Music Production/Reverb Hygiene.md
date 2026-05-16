This section will discuss common reverb problems and mistakes producers make.

### Problem: Harmonic Mud
When the chords change but the reverb still rings out and muddies up the spectrum.

### Solution: Automate the reverb on and off

1. Make a group with the Dry and reverb.
2. Map the reverb on to the reverb on and off. Make the range 127-127 and automate.
3. Add a utility and map it to the same macro.
4. Add a 0.5 second reverb to glue everything together
5. Multiband Compress

![[Harmonic Mud Solution.png]]

### Problem: Reverb sounds boomy, metallic

### Solution: EQ your Reverb chain

This is almost always necessary. Remove mud by using a high pass at 300-600 Hz, make it less metallic by adding a low pass at 10k. **Note that most plugins EQ have a post reverb EQ so make sure you EQ before.** This is the Abbey Road reverb trick.

### Problem: Making a Truly Ducking Reverb

### Solution: Noise Trigger 
Group the instrument with a short noise burst. Side chain compress the reverb with the noise trigger.

![[Noise Trigger Solution.png]]
### Problem: Reverbs and plucks don't got well together.
They create unnecessary noise that can kill the clarity.
           
### Solution: **process only the sustain.** 
Group the instrument with a short noise burst. Side chain compress the reverb with the noise trigger, and make sure you remove the transient. You can also use for phasers, flangers.

- You can process only the transient by swapping the compressor with a gate.



---


[[Dispersion]]
[[The Fake Mic (and more reverb tricks)]]
[[Music Production/index|Back]]