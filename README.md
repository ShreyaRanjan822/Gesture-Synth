# Gesture Synth

Play chords with your hands. Gesture Synth uses your webcam to track both hands and turns finger shapes, tilt, and height into a live chord instrument. Everything runs in the browser, and no video leaves your device.

**Live demo:** [https://gesture-synth-s.netlify.app/]

## How to play

Allow camera access, click **Start playing**, and hold both hands up to the camera.

### Left hand: the chord

| Gesture | Result |
|---|---|
| 1 to 5 fingers | Chords I to V |
| Index + pinky | Chord VI |
| Index + pinky + thumb | Chord VII |
| Lean fingers toward the center of the screen | Major |
| Lean fingers away from the center | Minor |

**Pitch shift:** turn on **Raise** or **Lower**, then move your left hand to the top half of the screen (raise one semitone) or the bottom fifth (lower one semitone). The middle plays the normal chord.

### Right hand: voicing and expression

| Gesture | Result |
|---|---|
| 1 finger | Root position |
| 2 fingers | First inversion |
| 3 fingers | Major 7th or minor 7th |
| 4 fingers | Dominant 7th or diminished 7th |
| Thumb in | Higher octave |
| Thumb out | Lower octave |
| Lean toward the center | More filter (darker sound) |
| Lean away from the center | Less filter (brighter sound) |
| Hand higher | Louder |
| Hand lower | Softer |

The right-hand finger count does not include the thumb.

## Example: "Sweet" by Cigarettes After Sex

Set the key to **F#**, then loop these left-hand chords:

1. 1 finger (F#)
2. 2 fingers, leaning away (G#m)
3. 4 fingers (B)
4. 5 fingers (C#)

## Run it locally

The camera only works over HTTPS or on `localhost`, so opening the file directly may not work. Serve the folder instead:

```bash
npx serve
```

Then open the address it prints in Chrome.

## Built with

- [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) for hand tracking
- [Tone.js](https://tonejs.github.io/) for sound
- Plain HTML, CSS, and JavaScript in a single file

## Notes

- Hand detection depends on lighting and how clearly your hands are visible, so you may need to adjust the thresholds in `index.html` for your setup.
- If your left and right hands feel swapped, change `SWAP_HANDS` at the top of the script.
- Inspired by [Gesture Synth](https://gesture-synth-weld.vercel.app/) by Eric Wei.
