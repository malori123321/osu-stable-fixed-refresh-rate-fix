# osu!stable — Fixed Refresh Rate / Visual Pacing Fix

A potential workaround for unusual visual pacing and approach-circle behavior in osu!stable using NVIDIA Profile Inspector.

## The problem

I experienced an unusual issue in osu!stable:

- Approach circles appeared to show up later than expected.
- Gameplay felt abnormally fast, even though the beatmap speed had not changed.
- Animations felt overly fast or unusually smooth.
- Mouse sensitivity was not the main issue.
- The game remained playable, but the visual timing felt different from what I was used to.

## What fixed it for me

Changing the following settings in **NVIDIA Profile Inspector** restored the familiar gameplay feel on my system.

### Settings

Open the `osu!` application profile and locate the G-SYNC settings.

| Setting | Value |
|---|---|
| GSYNC - Application Requested State | Fixed Refresh Rate |
| GSYNC - Application State | Fixed Refresh Rate |

Then click **Apply Changes** and restart osu!stable.

### My test environment

- Laptop: ASUS TUF Dash F15 FX516PC
- GPU: NVIDIA GeForce RTX 3050 Laptop GPU
- Integrated GPU: Intel Iris Xe Graphics
- Game: osu!stable
- Display refresh rate: 144 Hz
- Compatibility Mode: Enabled

## Result

On my system, the difference was immediately noticeable.

After applying Fixed Refresh Rate, osu!stable felt like it used to:

- Approach-circle behavior felt normal again.
- The unusual fast-paced visual feeling disappeared.
- Gameplay remained smooth.
- I did not need to change mouse sensitivity.

## Possible explanation

The improvement may be related to variable refresh rate configuration, frame presentation, or driver-level display synchronization.

However, this is a personal observation, not a verified root-cause analysis.

**These settings do not change the beatmap's actual Approach Rate, playback speed, or hit timing.**

The workaround may have no effect on systems without an active G-SYNC or compatible variable refresh rate display path.

## How to revert

1. Open NVIDIA Profile Inspector.
2. Select the `osu!` profile.
3. Restore the original values of both G-SYNC settings.
4. Click **Apply Changes**.
5. Restart osu!stable.

Export your original NVIDIA profile before making changes.

## Community testing

If you experience similar symptoms, please test this workaround and report:

- GPU model
- Display refresh rate
- Whether G-SYNC / VRR is supported and enabled
- osu!stable Compatibility Mode status
- Whether the workaround made a difference

This is an unofficial community workaround and is not affiliated with NVIDIA or osu!.
