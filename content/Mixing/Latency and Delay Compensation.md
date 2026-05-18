When we record audio through an audio interface, audio information comes as an analog signal, and is being converted to a digital signal, so that the computer can read it. The process is called AD conversion. That same process happens so that we can hear audio through our speakers or headphones, just in reverse. And it is called, shocker, DA conversion.

That whole roundtrip takes a little bit of time. For us listening its unnoticable, but for recording musicians its very noticable. Anything larger than 8-10ms will make recording very hard for the performer.

### Things that affect Latency
 - Your Audio interface
 - Your CPU
 - Your DAW's buffer size
 - Plugins

> Most audio interfaces today have a direct monitoring option to combat latency while recording.

> When you're recording in Ableton, turn on **Reduced Latency When Recording** in the options menu.

![[Ableton Low Latency Mode.png|388]]



### Delay Compensation
Ok, latency is bad, but we're not performing right? Why do we care if we're only mixing?

Remember how we said that plugins cause latency? Different plugins bring with them different amounts of latency, and that could bring our whole project out of sync. Fortunately, DAWs today have a function called **delay compensation** that deals with that problem for you. **Make sure it’s turned on In ProTools.** 

In Ableton, you can directly change tracks delay if you enable **Track Options** in the arrangment tracks under the view menu.

![[Ableton Track Options.png]]

___

[[Session Setup]]
[[Panning]]
[[Mixing/index|Back]]