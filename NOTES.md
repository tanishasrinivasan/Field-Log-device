# Offshore technician field recorder

## Current design
- `main.kcl` is the assembled entrypoint. `explodedOffset = 0mm` is assembled; 28 mm separates the parts for review.
- Vertical enclosure: **105 mm high × 60 mm wide × 24 mm deep**, including the raised front perimeter, excluding the belt clip and side-button projection. Plan corners are R10. Rear tray is 14 mm deep; front shell extends another 10 mm. Nominal skins/walls remain 2 mm with locally reinforced mounts.
- The working front surface is at z=22 mm, recessed 2 mm below the continuous perimeter. The Ø38 mm record button has a true revolved spherical dish, 2 mm deep over Ø34 mm, with a 2 mm wide rim. Its rim is at z=23.8 mm, below the perimeter. A concentric Ø42 mm housing surround rises 0.6 mm above the working face.
- Top status window: 38 × 18 mm with a neutral raised bezel framing a 34 × 14 mm visible area. Static `A-104` sits above a balanced time/REC row with a neutral status dot. These are illustrative graphics, not functional electronics.
- Graphite 32 × 10 mm FLAG control with R4.8 pill corners, centered single-line legend and matching R5.1 clearance opening; separate retained cap. The 8 × 30 mm side paddle retains R3.8 corners, five grip bars, original flange and projection. Assembly appearance overrides its standalone amber finish to graphite.
- Assembled housing uses one neutral graphite color; secondary controls, clip and grille are dark graphite. Orange is reserved for the concave record cap. Existing component centers and internal packaging remain unchanged.
- Lower front: replaceable 34 × 12 mm microphone grille with four rounded 27 × 1.4 mm slots on 2.4 mm pitch. A separate 0.3 mm acoustic backing allowance is provided behind it; acoustic performance and a sealed material system are not established.
- Bottom USB-C clearance opening retains the requested 10 × 4 mm size; no connector, port cover, or charging electronics are detailed.
- Rear: reinforced 30 × 54 mm removable belt/vest clip on an upper mounting root, with retention toe and two internal stiffening ribs. It ends above the lower scanning label, leaving the scanning zone uncovered. Clip projects 7.5 mm behind the housing: assembled overall depth is 31.5 mm. Side paddle ribs project 1.7 mm beyond the nominal width.
- Lower rear: flat 38 × 30 mm nonmetallic scan-target patch marked **NFC / TAP / EQUIPMENT**. The label is 0.25 mm thick, with 0.04 mm geometric ink strokes. Scan operation while clipped to clothing still requires ergonomic/RF verification.

## Retained and revised interfaces
- Four Ø7 mm screw pillars moved to x=±22, y=±44. Rear Ø2.8 clearance bores and Ø5.2 × 1.4 mm head pockets; front Ø2.05 blind M2.5 pilot allowances. Pilot fit must be tested with actual screws and printed material. Fasteners and helical threads are not modeled.
- Clip mounting pilots are x=±9, y=42 in a reinforced internal pad.
- The earlier Ø20 × 3 mm magnet pocket is retained but relocated to the upper rear at (0,20), beneath the removable clip and away from the labeled scan target. It has 2 mm backing. No magnet is installed in the CAD model; RF compatibility remains unverified.
- Earlier standalone LED/light-pipe placement is superseded by the status display. `lightPipe.kcl` is preserved but is no longer imported into the assembly.

## Internal packaging — provisional envelopes, not detailed electronics
| Envelope | X × Y × Z, mm | Assembled center X,Y | Lower Z |
|---|---|---|---|
| Compact headerless ESP32 | 26 × 40 × 6 | 0,21 | 6 |
| Compact PN532 | 42 × 40 × 3 | 0,-20 | 2.5 |
| LiPo | 32 × 30 × 5 | 0,-20 | 6.5 |
| I2S MEMS mic | 14 × 10 × 2 | 0,-41 | 16 |

The original envelope definitions are unchanged, but their assembly locations now match the vertical layout and lower microphone/scan zones. Select actual boards, cell, switches, display and USB hardware before fixing mounts, connector access, wiring, cell swelling clearance or battery capacity. No universal ESP32 fit or 500–1000 mAh cell fit is claimed.

## Validation and limitations
- All edited physical-part sketches, including the concave cap and stroke graphics, executed fully constrained. Part-level aperture checks and assembled/exploded visual reviews passed. The record-button module exposure was corrected so the assembled cap is placed on the front, not left at the origin.
- Some shell/grille/paddle booleans use the working KCL 2.0 legacy algorithm and emit deprecation warnings. The final assembled entrypoint executes without errors.
- Separate manufactured parts remain separate. Label/display strokes are graphic bodies aggregated with their host parts for assembly placement; they represent printing/display pixels, not independently manufactured items.
- Shared dimension-driven profiles and hand-defined stroke glyphs use functions. Sketches inside those functions are code-editable, not point-and-click editable. The main concave cap profile remains a top-level editable solver sketch.
- Shell joint remains a screw-clamped butt joint. Gasket system, USB sealing, switch return/sealing mechanisms, component retainers, clip fatigue, salt-spray/drop testing and RF qualification remain engineering work.
- This is a ruggedized CAD design, **not a qualified offshore product**. No IP, intrinsic-safety, hazardous-area, impact, or load rating has been established.
- For fabrication preparation, select physical part files rather than printing clearance envelopes or treating illustrative ink strokes as structural solids.
