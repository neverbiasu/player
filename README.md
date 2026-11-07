# Real-camera checks after roll fix (issue #4)

Reporter: neverbiasu. Date: 2026-11-07. Character: Nana / d03ft. Browser UA: Chrome 156; macOS 15.3.

Fix commit: c08382c, based on 95b663ec492a7ee72440cedca7a60558de259c7a. The manual record identifies the exact source patch by SHA-256: 5dae01523a33de1c1eb72bf8644b7f727294d1077c6b6a6a093f4dd49681f35c.

| mirror | Physical motion | Expected / reporter-confirmed output |
|---|---|---|
| true | Tilt toward my left shoulder | Screen-left |
| true | Turn my face left | Screen-left |
| false | Tilt toward my left shoulder | Screen-right |
| false | Turn my face left | Screen-right |

The reporter personally completed the real-webcam checks and answered "All four cases correct; evidence downloaded." The original JSON still marks the two mirror=true cases as unclear. It is preserved unchanged; the separate clarified JSON records the reporter's subsequent answer to a question that explicitly specified the expected directions above. These are manual observations and timestamps, not recorded MediaPipe traces. Screenshots contain only the character canvas, with no webcam image of a person.

Before-fix evidence and the maintainer's confirmation: https://github.com/livliv-dev/player/issues/4

The images are original, unedited downloads. SHA256.json records their hashes and those of the two manual records. This independent evidence branch is not part of the code-fix PR diff.
