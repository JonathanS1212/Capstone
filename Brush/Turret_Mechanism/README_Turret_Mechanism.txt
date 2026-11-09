TURRET MECHANISM - parts that make Concept A / B actually work
==============================================================
Frame: hub centre = origin, axle = Y axis, boom/bracket on -Y. Heads radial in XZ.
Window (working) head points +Z. Home = head 1 in the window, magnet over the Hall sensor.

WHAT EACH PART DOES
1. Rotation + homing
   T01 Axle_Long (6 mm steel, 59.6 mm), T08 DriveMotorMount (clamps the outer end of
   the TipBracket boss), T09 ShaftCoupler (6 mm -> 3 mm), N20 gearmotor with encoder.
   Home: 3x2 mm magnet in the hub + Hall sensor in the stator plate. Turret travel is
   limited to 0..288 deg (5 positions), so no slip ring is needed.
2. Wiring through a rotating hub
   Each head: wires exit the shoulder toward -Y through a silicone grommet, run in a
   groove on the hub's back face to a 3-pin connector (HV, motor+, GND).
   The 15-wire bundle (30 AWG silicone, HV wire for the electrode lines) passes onto
   T03 CassetteRotor and is wound 1.5 turns as a loose "clock spring" inside the stator
   drum, then leaves at the bottom (4 mm hole) to the pod. 288 deg of travel only
   winds/unwinds the spiral; nothing slides.
3. Idle-head covers (no actuator needed)
   T05 Stator = clamp collar + cassette drum + cam plate, one printed part, fixed to the
   bracket. Each sleeve carries a 1.5 mm pin running in the plate's cam groove: as the hub
   turns, the groove pulls the window head's sleeve back 8-10 mm and pushes the other
   four forward over their brushes/swabs. Positive cam both ways, no springs.
4. Grounding whisker
   1 mm carbon rod + carbon tuft clamped in a block on the stator rim at the window,
   reaching 4-5 mm past the active tip so it touches the plant first. Wire it to pod GND.
5. Retention
   MotorClipB snaps over the window of Concept B's motor pocket (barbs in notches).
   Grommets A/B strain-relieve the head leads. Concept A's motor is enclosed in the bore.
6. Electronics pod (on the 30 mm boom, strapped)
   +800 V and -1 kV HV modules, 8 reed relays (K1 +800 V, K2 -1 kV, K3 discharge,
   K4-K8 head select), MCU, motor driver + 5 MOSFETs, 5 V regulator.

CHANGES TO EXISTING TEAM PARTS
 - TipBracket "Turret Offset" 16 -> 28 mm (and Axle Length 47.6 -> 59.6 mm).
 - Hub_Turret is replaced by T02_Hub_Wired (same 33 x 14 mm, adds grooves/pockets/screws).
 - Head spigot D-flat moved to the -Y side (hub screw now comes in axially from the back).
 - Head wire exits moved to z = 2 mm, toward -Y. Updated head files are included.
 CHECK: the drive-motor rails sit at x = +/-10 mm; make sure they clear the bracket's arm
 socket, and that the stator plate (67 mm) clears the arm. Socket direction was not in
 the variables files.

FILES
 Turret_ConceptA_Assembly.step / Turret_ConceptB_Assembly.step: everything in place.
   Parts ending in _env are bought-part envelopes. REF_ = existing team part, for context.
 ElectronicsPod_Assembly.step
 Parts_STEP / Parts_STL: printable / machinable parts (STL only for printed ones).
 All sizes are first-pass estimates to rebuild in SolidWorks from the Variables file.
 Interference check: no clashes except intended ones (swab on wire, tuft on rod).
