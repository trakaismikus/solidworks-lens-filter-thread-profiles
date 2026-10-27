# SOLIDWORKS Thread Profiles for Camera Lens Filter Threads

Custom **SOLIDWORKS thread profiles** (`.SLDLFP`) for **camera lens filter threads**: 48 common
photo and video filter sizes, from M19x0.5 to M122x1.0 (M52x0.75, M58x0.75, M62x0.75, M67x0.75,
M72x0.75, M77x0.75, M82x0.75 and others).

Use them with the SOLIDWORKS **Thread** feature (Insert > Features > Thread) to model:

- lens caps, filter holders, hoods and step-up / step-down rings
- 3D-printed filter adapters and lens adapters
- telescope and microscope camera adapters with filter threads

The standard SOLIDWORKS *Metric Tap* and *Metric Die* profiles only have coarse and common fine
pitches. They do not have the fine 0.5 mm and 0.75 mm pitches that lens filters use. These
files add them.

## Files

| File | Thread | Use it for |
|---|---|---|
| `Lens Filter Tap.SLDLFP` | Internal (female) | The front of a lens, the inside of a filter ring, the inside of a step ring |
| `Lens Filter Die.SLDLFP` | External (male) | The back of a filter, a lens cap that screws in, the outside of a step ring |

Both files are made from the SOLIDWORKS 2021 *Metric Tap* and *Metric Die* profiles. The thread
shape is the ISO metric 60° profile. Only the pitch changes from size to size:

| | Tap (internal) | Die (external) |
|---|---|---|
| Thread angle | 60° | 60° |
| Profile height | 0.5413 × P | 0.5413 × P |
| Flat (land) | P / 8 | P / 4 |

## Thread sizes

Each size is a configuration in both files. The name is `M<diameter>x<pitch>`, in millimetres.
Some diameters come in two pitches (for example `M37x0.5` and `M37x0.75`). Check your part
before you pick one.

| Size | Diameter (mm) | Pitch (mm) | Note |
|---|---|---|---|
| M19x0.5 | 19 | 0.5 | Very rare |
| M24x0.5 | 24 | 0.5 | Very rare |
| M25x0.75 | 25 | 0.75 | |
| M25.5x0.5 | 25.5 | 0.5 | Very rare |
| M27x0.5 | 27 | 0.5 | Frequent, video cameras |
| M27x0.75 | 27 | 0.75 | Very rare |
| M28x0.75 | 28 | 0.75 | Very rare |
| M28.5x0.5 | 28.5 | 0.5 | Astronomy 1.25" eyepiece filters |
| M28.5x0.75 | 28.5 | 0.75 | Very rare |
| M30x0.75 | 30 | 0.75 | |
| M30.5x0.5 | 30.5 | 0.5 | |
| M30.5x0.75 | 30.5 | 0.75 | |
| M34x0.5 | 34 | 0.5 | Very rare |
| M35x0.5 | 35 | 0.5 | Very rare |
| M35.5x0.5 | 35.5 | 0.5 | Frequent, video cameras |
| M36.5x0.5 | 36.5 | 0.5 | |
| M37x0.5 | 37 | 0.5 | |
| M37x0.75 | 37 | 0.75 | |
| M37.5x0.5 | 37.5 | 0.5 | |
| M38x0.75 | 38 | 0.75 | Very rare |
| M39x0.5 | 39 | 0.5 | Video cameras, Leica E39 |
| M40x0.5 | 40 | 0.5 | Very rare |
| M40.5x0.5 | 40.5 | 0.5 | Frequent, video cameras |
| M41x0.5 | 41 | 0.5 | Very rare |
| M43x0.5 | 43 | 0.5 | Very rare |
| M43x0.75 | 43 | 0.75 | |
| M45x0.5 | 45 | 0.5 | |
| M46x0.75 | 46 | 0.75 | |
| M48x0.75 | 48 | 0.75 | Also astronomy 2" filters |
| M49x0.75 | 49 | 0.75 | Frequent |
| M52x0.75 | 52 | 0.75 | Very frequent |
| M55x0.75 | 55 | 0.75 | Frequent |
| M58x0.75 | 58 | 0.75 | Very frequent |
| M60x0.75 | 60 | 0.75 | |
| M62x0.75 | 62 | 0.75 | Very frequent |
| M67x0.75 | 67 | 0.75 | Very frequent |
| M69x0.75 | 69 | 0.75 | |
| M72x0.75 | 72 | 0.75 | Very frequent |
| M75x0.75 | 75 | 0.75 | Rare |
| M77x0.75 | 77 | 0.75 | Very frequent |
| M82x0.75 | 82 | 0.75 | Frequent |
| M86x1.0 | 86 | 1.0 | Also called C86 |
| M95x1.0 | 95 | 1.0 | Also called C95 |
| M100x0.75 | 100 | 0.75 | |
| M100x1.0 | 100 | 1.0 | |
| M105x1.0 | 105 | 1.0 | Also called C105 |
| M112x1.5 | 112 | 1.5 | |
| M122x1.0 | 122 | 1.0 | |

Size list and notes from the
[gewindebohrer.de photo thread table](https://www.gewindebohrer.de/en/service/thread-standards/thread-in-the-photo-area).
Sources do not agree on all large sizes. Some 86 mm and 95 mm filters use a 0.75 mm pitch.
Measure your part if you are not sure.

## How to install

1. Download `Lens Filter Tap.SLDLFP` and `Lens Filter Die.SLDLFP`
   (click the file, then click **Download raw file**).
2. Find your thread profiles folder. In SOLIDWORKS, go to
   **Tools > Options > System Options > File Locations**. Select **Thread Profiles** in the list.
   The default folder is:

   ```
   C:\ProgramData\SOLIDWORKS\SOLIDWORKS <version>\Thread Profiles
   ```

   `C:\ProgramData` is a hidden folder. Type the path into the File Explorer address bar.
3. Copy the two files into that folder. Do not replace or delete the files that are there.
4. If SOLIDWORKS is open, close it and open it again.

## How to use

1. Make a cylinder (for an external thread) or a hole (for an internal thread) at the size of
   the thread. For example, 52 mm for M52x0.75.
2. Go to **Insert > Features > Thread**.
3. Select the circular edge where the thread starts.
4. In **Specification > Type**, select **Lens Filter Die** (external) or
   **Lens Filter Tap** (internal).
5. In **Size**, select the thread, for example `M52x0.75`.
6. Set the thread length and click OK.

For 3D printing, make the internal thread a little larger. Use **Override diameter** and add
0.1–0.3 mm. The correct value depends on your printer.

## Compatibility

- Saved in SOLIDWORKS 2021 (the Thread feature was added in SOLIDWORKS 2016).
- The files open in SOLIDWORKS 2021 and newer. Older versions cannot open them.

## Keywords

SOLIDWORKS thread profile, SLDLFP, custom thread profile, lens filter thread, camera filter
thread, filter thread pitch 0.75 mm, filter thread pitch 0.5 mm, M52x0.75, M58x0.75, M62x0.75,
M67x0.75, M72x0.75, M77x0.75, M82x0.75, M49x0.75, M55x0.75, M40.5x0.5, M37x0.75, step-up ring,
step-down ring, lens cap, filter adapter, 3D print lens thread, fine metric thread SOLIDWORKS.
