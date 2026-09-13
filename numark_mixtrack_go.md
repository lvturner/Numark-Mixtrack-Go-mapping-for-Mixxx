# Numark Mixtrack Go



**Numark Mixtrack Go** is a USB [MIDI](https://manual.mixxx.org/2.5/en/glossary#term-MIDI) controller with an integrated audio interface.
It improves on the concept of the Numark DJ2GO2 Touch by adding:

- STEMS tracks support - the STEMS support in [Mixxx](https://mixxx.org/download/) is added on version 2.6.
- Shifting - now some buttons have alternate actions if pressed while shifted.
- Mode selection is independent for each deck.
- Better LED feedback.
- More controls.

Useful links:
- [Numark Mixtrack Go website](https://www.numark.com/new/mixtrack-go/)
- [Mixxx forum thread for this mapping](https://mixxx.discourse.group/t/numark-mixtrack-go-mapping/34099)

The Numark Mixtrack Go controller is a USB Audio and MIDI Class compliant device and works with Linux, macOS, and Windows.


## Soundcard Setup

This controller has a built-in 4 channel output sound card, with a stereo Main output (3.5mm jack) and stereo Headphone output (3.5mm jack).

- To configure the controller's sound card:
   - Open **Preferences** > **Sound Hardware**
   - Select the **Output** tab.
   - From the **Main** drop-down menu, select the audio interface, then **Channels 1-2**.
   - From the **Headphones** drop-down menu, select the audio interface, then **Channels 3-4**.
   - Click **Apply** to save the changes.




## Controller Layout

- The Numark Mixtrack Go's layout has 3 sections:
  - The middle holds the mixer related controls, library browsing and track loading controls.
  - On each side there is a deck control area, where in Mixxx the left deck control will control Deck 1 and the right deck will control Deck 2. Each side can be switched to control the other deck of its pair (left: Deck 1 or 3, right: Deck 2 or 4) by holding the {hwlabel}`HEADPHONE` button and pressing {hwlabel}`PAD 1` on the left or {hwlabel}`PAD 2` on the right.
  - Both decks have essentially the same controls each. What differs is that the left side also has the connector to the Main Output and on the right side there's both a USB-C plug and Headphones connector.

![alt text](../../_static/controllers/numark_mixtrack_go_full.svg "Title")


## Mixer Area Layout

![alt text](../../_static/controllers/numark_mixtrack_go_mixer.svg "Title")


```{list-table}
:header-rows: 1
:align: center

* - Number
  - Control
  - Function
* - **1**
  - {hwlabel}`BROWSER`
  - A knob for browsing the Library. If pushed, loads a track on the Preview Deck.
* - **2**
  - {hwlabel}`LOAD`
  - Each button loads a track to the Deck on their side (with a short delay, so that a combined press can be detected). Pressing **both {hwlabel}`LOAD` buttons together** toggles the mixer knobs between Filter mode and EQ mode (see {hwlabel}`MAIN LEVEL`, {hwlabel}`CUE LEVEL` and {hwlabel}`LEVEL` below). The button LEDs stay on while in EQ mode.
* - **-**
  - {hwlabel}`SHIFT` + {hwlabel}`LOAD 1`
  - Switches the {hwlabel}`FILTER/LOW` knobs between controlling the channels Quick Effect and the Low EQ.
* - **-**
  - {hwlabel}`SHIFT` + {hwlabel}`LOAD 2`
  - Toggles the Vinyl mode in the Jogwheel.
* - **3**
  - {hwlabel}`BLUETOOTH`
  - There is currently no functionality for this LED in Mixxx.
* - **4**
  - {hwlabel}`MAIN LEVEL`
  - Controls the Main Output Gain. In EQ mode (both {hwlabel}`LOAD` buttons), controls the High EQ of the left deck (Deck 1 or 3).
* - **5**
  - {hwlabel}`CUE LEVEL`
  - Controls the Headphone Gain. In EQ mode (both {hwlabel}`LOAD` buttons), controls the High EQ of the right deck (Deck 2 or 4).
* - **6**
  - {hwlabel}`LEVEL`
  - Controls each channel's Volume. In EQ mode (both {hwlabel}`LOAD` buttons), controls the Mid EQ of the deck on that side (Deck 1 or 3 on the left, Deck 2 or 4 on the right).
* - **7**
  - {hwlabel}`FILTER/LOW`
  - Controls the Quick Effect currently selected for that channel, or the Low EQ. Outside of EQ mode, use {hwlabel}`SHIFT` + {hwlabel}`LOAD 1` to switch between the Effect and Low EQ. In EQ mode (both {hwlabel}`LOAD` buttons), always controls the Low EQ. Select the Effect in the Mixxx graphical interface.
* - **8**
  - {hwlabel}`HEADPHONE`
  - Sends that channel's audio through the Headphone Output. The button latches, toggling the cue on release; a quick tap acts as usual. Hold this button and press {hwlabel}`PAD 1` (left side) or {hwlabel}`PAD 2` (right side) to switch that side's deck between its pair: Deck 1 <-> 3 and Deck 2 <-> 4. The pad lights up while held and flashes briefly on release to confirm the change, then the pads, jogwheel and the mixer knobs control the other deck, and the active Pad Mode LED blinks to show that the deck is on its secondary channel. This combo does not toggle the headphone cue. Pressing {hwlabel}`PAD 1` or {hwlabel}`PAD 2` while holding the {hwlabel}`HEADPHONE` button resets the pad mode to Hotcue.
* - **9**
  - {hwlabel}`FADE FX`
  - This button toggles the Fade FX feature in Mixxx. When Fade FX is active, moving the Crossfader away from the current deck will activate the Quick Effect of that deck. When inactive, the Crossfader will work normally.
* - **10**
  - {hwlabel}`CROSSFADER`
  - Fades between the Left and the Right channel.
```

```{note}
   - While Fade FX can use any effect available on each channel, effects that don't have their reset point at 0
     (when the knob is turned all the way to the left), may not work as expected.
   - These effects currently are:
       - Filter Echo
       - Mid/Side
       - Balance
       - Filter
       - Loudness
       - Moog Filter
       - Pitch Shift
```

## Deck Area Layout

![alt text](../../_static/controllers/numark_mixtrack_go_deck1.svg "Title")


```{list-table}
:header-rows: 1
:align: center

* - Number
  - Control
  - Function
* - **11**
  - {hwlabel}`JOGWHEEL`
  - If Vinyl Mode is active, the top surface controls scratching and the side surface controls Pitch Bend. If Vinyl Mode is inactive, both surfaces control pitch bend. Use {hwlabel}`SHIFT` + {hwlabel}`LOAD 2` to toggle.
* - **12**
  - {hwlabel}`TEMPO FADER`
  - Changes the track's playback speed.
* - **13**
  - {hwlabel}`MAIN AUDIO OUTPUT`
  - Connect this output to an amplifier or speaker system. This main out put volume is controlled by the {hwlabel}`LEVEL` knob.
* - **14**
  - {hwlabel}`ACAPEL`
  - The Acappella button activates an acappella from the loaded track. This is a STEMS button.
* - **15**
  - {hwlabel}`INSTRU`
  - The Instrumental button activates an instrumental from the loaded track. This is a STEMS button.
* - **16**
  - {hwlabel}`CUE`
  - Sets the cue point or moves to the main cue point and stops. See options at **Preferences** > **Deck** > **Cue mode**.
* - **-**
  - {hwlabel}`SHIFT` + {hwlabel}`CUE`
  - Moves to the main cue point and resumes playing from there.
* - **-**
  - {hwlabel}`SHIFT` + {hwlabel}`CUE`(2x)
  - Loads the previous track on the Library and starts playing it from the main cue point. This action is prevented if **Preferences** > **Deck** > **Loading a track, when a deck is playing** is set to Reject.
* - **17**
  - {hwlabel}`SYNC`
  - Long Press to activate Sync Lock. Tap to trigger beat sync (syncs tempo and phase).
* - **18**
  - {hwlabel}`PLAY/PAUSE`
  - Plays or Pauses the track.
* - **-**
  - {hwlabel}`SHIFT` + {hwlabel}`PLAY/PAUSE`
  - Moves to the main cue point and resumes playing from there. Same as Shift + Cue.
```
```{note}
   {hwlabel}`ACAPEL` and {hwlabel}`INSTRU` functions require a STEMS track to be loaded and a MIXXX version 2.6 or higher.
```

![alt text](../../_static/controllers/numark_mixtrack_go_deck2.svg "Title")

```{list-table}
:header-rows: 1
:align: center

* - Number
  - Control
  - Function
* - **19**
  - {hwlabel}`USB-C PORT`
  - This port serves as both source of power and data transfer to and from your computer or other device.
* - **20**
  - {hwlabel}`HEADPHONE OUTPUT`
  - Connect headphones to this 1/8” (3.5 mm) jack for monitoring a channel. The headphone volume is controlled using the {hwlabel}`CUE LEVEL` knob.
* - **21**
  - {hwlabel}`MODE` (**SHIFT**)
  - Press this button to change the current function of the Performance Pads. A long press activates the **SHIFT** functions on other controls.
* - **22**
  - {hwlabel}`MODE LEDS`
  - These LEDs highlight the current pad mode. The modes cycle in the order HOT CUE->LOOPS->FX->SAMPLER->STEMS. The FX mode is activated when both the LOOPS and the SAMPLER LEDs are highlighted.
* - **23**
  - {hwlabel}`PADS`
  - Performance Pads: These pads can be used to trigger Hotcues, Loops, Samples, Stems, and to apply effects. To change the function of the pads, press {hwlabel}`MODE`.
* - **-**
  - **Hotcue Mode**
  - In Hotcue Mode, a Pad sets a hotcue in the current position of the track. {hwlabel}`SHIFT` + {hwlabel}`PAD` clears the corresponding hotcue.
* - **-**
  - **Loops Mode**
  - In Loops Mode, Pads 1, 2, 3 and 4 set 1, 2, 4 and 8 beat sized beatloops respectively. {hwlabel}`SHIFT` + {hwlabel}`PAD` clears the corresponding beatloop.
* - **-**
  - **FX Mode**
  - In FX mode, {hwlabel}`PAD1` starts an Echo Effect, {hwlabel}`PAD2` starts a Flanger Effect, {hwlabel}`PAD3` starts a Reverb Effect and {hwlabel}`PAD4` starts a 1 beat sized beatroll.
* - **-**
  - **Sampler Mode**
  - In Sampler Mode, each pad loads the currently selected track in the library into it's sampler. If it is already loaded, it starts playing the sample until the sample ends. {hwlabel}`SHIFT` + {hwlabel}`PAD` ejects the track from the corresponding sampler.
* - **-**
  - **STEMS mode**
  - In STEMS Mode, pads mute and unmute the components of the loaded STEMS track: {hwlabel}`PAD1` affects the Drums stem part, {hwlabel}`PAD2` affects the FX/Bass stem part, {hwlabel}`PAD3` affects the Synth stem part and {hwlabel}`PAD4` affects the Voice stem part.
```
```{note}
   **STEMS mode** functionality requires a STEMS track to be loaded and a MIXXX version 2.6 or higher.
```
