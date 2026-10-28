# TOUCH BLOOP

<img src="touch.jpeg" width="300"/>

## ABOUT
Bloop is a glitch looper for the Simple Touch, inspired by the legendary Chase Bliss Blooper pedal. It all started when Chase Bliss asked us to take part in their Mystery Box (2026 edition!). We wanted to make something special for the occasion, so Roey and Vlad started working on a new glitch / beat-repeat / looper thing. In a sense, it's a micro [Spotykach](https://synthux.academy/store/spotykach).

## QUICK START
1. Plug an instrument, a radio, your phone or anything else into the input.
2. Turn the **MIX** knob (bottom right) all the way up.
3. Touch any of the pads. Bloop grabs what's playing and loops it straight back at you.
4. Each pad puts a different distortion on the loop. The **centre pad** leaves it clean.
5. Use the **left fader** to morph the distortion from digital (down) to analog (up).

That's it! Now use the knobs to change the loop's **size**, **position** and **pitch**, add **mod (modulation)** and **reverb**, and use the **right fader** to filter it: low-pass at the bottom, high-pass at the top, open in the middle.

Enjoy Blooping!

## INSTALL
Flash it from the [Synthux firmware tool](https://synthux.academy/firmware) (Touch → TouchBloop), or download the `.bin` from the [latest release](https://github.com/Synthux-Academy/TouchBloop/releases/latest) and flash it with the [Daisy web programmer](https://electro-smith.github.io/Programmer/).

## THE PADS
Hold a pad to loop. Hold several and the loop keeps going while the last pad you touched sets the distortion, so you can play the effects like a drum.

## THE LEFT FADER: DIGITAL ↔ ANALOG
The left fader (DISTORT) changes the character of every pad except the clean centre one.

- **Down, digital:** fewer bits and a lower sample rate make it gritty, broken and lo-fi. The wah is parked low and the fold barely touches the sound.
- **Up, analog:** the crush clears away. The wah pads open up and get vocal, and the fold pads fold harder and get thicker and brighter.
- **In between:** a bit of both.

Every pad has its own sweet spot. **Hold a pad and slide the fader slowly up and down** to hear it change shape, then try the next pad.

## THE SWITCHES
**Right switch: how the pads play**
- **Centre, Momentary:** a loop plays while you hold a pad and stops when you let go.
- **Up, Latch:** tap a pad and the loop keeps going after you let go. Tap another pad to restart it, or hold one and tap another to change only the distortion.
- **Down, Effects only:** no loops. A held pad puts its distortion straight on whatever is coming in.

**Left switch: which way the loop plays**
- **Up, Forward:** every pass plays forward.
- **Centre, Random:** each pass plays forward or backward at random.
- **Down, Reverse:** every pass plays backward. It's best flipped while a loop is already playing.

## TIPS
- **Keep MIX all the way up** for the full glitch: the loop replaces your input while it plays. Turn it down and the dry input comes back underneath.
- **Sound has to be coming in when you touch.** If you touch in a silent gap nothing happens: let go and touch again.
- **Play the pads like a drum.** Hold one pad and tap the others to jump between distortions without stopping the loop.
- **Flip the direction switch while a loop plays** to turn it backwards on the fly.
- **Hold TO or CH while turning PITCH** to snap the loop to fifths and octaves, so it stays in key.
- **Switch the pads to Effects only** to use Bloop as a hand-played distortion box on whatever comes in.
- **Hidden functions wait for you.** While TO or CH is held, a knob's hidden function takes over only once the knob passes where it was last set (the main function does the same when you let go), so nothing jumps.

## ALL CONTROLS
Hidden functions: hold **TO** or **CH** (either one) while you turn the knob.

**Knobs and faders**

| Control | Name | Function | Hidden function (TO or CH) |
|---|---|---|---|
| S30 | SIZE | Loop length, from 50 ms to 5 s | – |
| S31 | POS | Where the loop sits in the 5 s recorded after you touch | – |
| S32 | PITCH | Speed and pitch together, like tape: from stopped to 2 octaves up. Just left of noon is normal speed | Snaps to a fifth, or one or two octaves, down or up |
| S33 | MOD | Blur: grains start a little early or late, smearing the loop | Tape flutter: wobbly pitch and a duller, worn-tape sound |
| S34 | REVERB | How much goes into the reverb | How long the reverb rings |
| S35 | MIX (bottom right) | From the dry input (down) to Bloop's loops, filter and reverb (up) | Output volume |
| S36 | DISTORT (left fader) | The pads' distortion, from digital (down) to analog (up) | – |
| S37 | FILTER (right fader) | Low-pass below the middle, high-pass above it, open in the middle. Filters the loops and the input | Input volume, up to +12 dB |

**Switches**

| Switch | Up | Centre | Down |
|---|---|---|---|
| S07/S08 · pads | **Latch:** a tap starts a loop and it keeps going. Tap another pad to restart it | **Momentary:** a loop plays while you hold a pad | **Effects only:** no loops, a held pad puts its distortion on the input |
| S09/S10 · direction | Forward | Random: each pass forward or backward | Reverse |

**Pads**

| Pad | Function |
|---|---|
| P00–P02 | Not used |
| P03–P09 | Loop + distortion (see [The pads](#the-pads)) |
| TO, CH | Hold for the knobs' hidden functions |

## BUILD IT YOURSELF
```shell
$ git clone --recurse-submodules https://github.com/Synthux-Academy/TouchBloop.git
$ cd TouchBloop
$ make libs
$ make
$ make program-dfu
```
