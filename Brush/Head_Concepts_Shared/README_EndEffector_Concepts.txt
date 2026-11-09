END-EFFECTOR HEAD CONCEPTS A AND B  (generated 2026-11-08)
=========================================================

Both heads replace Brush/Head(Placeholder).SLDPRT on the five-arm turret hub.

INTERFACE (taken from Hub_Turret and Axle_Turret variables)
- Spigot: dia 6.0 mm x 10 mm, goes into the hub socket (Hub: Spigot Hole 6.2, Socket Depth 10).
- 0.5 mm D-flat, 8 mm long, for the hub set screw (Hub: Set Screw Hole 2.5).
- Shoulder: dia 10 mm x 4 mm, seats on the hub outer surface (hub dia 33 mm).
- Part origin: z = 0 at the shoulder face; head axis = +Z; spigot is z = -10 to 0.

CONCEPT A - CHARGED PROBE  (folder ConceptA_ChargedProbe)
- A01 ProbeBody      resin print: dia 8 x 32 mm body, 6.0 motor bay, 6.6 front bore, step for bulkhead, radial wire hole dia 2.6 at 8 mm
- A02 FrontCollar    resin print: dia 10 ring over the body front, 1 mm-wide x 2 mm-deep bristle groove
- A03 Bulkhead       resin print: dia 6.55 x 1.2 disc, dia 3.6 centre hole, dia 1.2 pad-wire hole
- A04 PadCopper      copper foil ring 6.4 / 4.0 mm (pad face sits 2 mm behind the brush root)
- A05 PadInsulation  polyimide tape layer over the pad
- A06 TuftTube       brass tube 3.0 / 2.5 x 10 mm
- A07 TuftSleeve     PTFE heat-shrink over the tube
- A08 CarbonTuft     carbon-fibre bristle bundle, simplified as a dia 2.5 rod; ends 1 mm past the brush
- A09 BrushRing      nylon bristles, simplified as a splayed conical shell (4 mm exposed, 14 deg splay)
- A10 VibrationMotor 4 x 8 mm pager motor envelope
Overall: tip of tuft 41 mm from the hub surface.

CONCEPT B - CHARGED FLOCKED SWAB  (folder ConceptB_ChargedSwab)
- B01 SwabHolder     resin print: dia 8 body, cone nose to dia 4, dia 1.7 core bore, open-sided motor cradle, M2 clamp-screw hole
- B02 CoreWire       brass wire dia 1.0 (electrode)
- B03 CoreSheath     PTFE heat-shrink dia 1.6
- B04 FlockedHead    flocked swab head envelope, dia 4 x 6 mm
- B05 VibrationMotor 4 x 8 mm pager motor envelope
Overall: tip of head 42 mm from the hub surface.

FILES
- <Concept>_Assembly.step   : all parts positioned (colour-coded)
- Parts_STEP/*.step          : one solid per part (open in SolidWorks: File > Open, type STEP)
- Parts_STL/*.stl            : for printing the resin parts (A01-A03, B01)
- *_Variables.txt            : SolidWorks equation file in the team's naming style, so the
                               parts can be rebuilt as parametric SLDPRTs (Tools > Equations >
                               Link to external file)
- *_Preview.png, *_Section.png/.svg : renders and half-section line drawings
- ConceptX_on_Turret_Preview.step (in this folder): five heads on a stand-in hub for context

IMPORTANT NOTES
1. These are STEP/STL files, not native .SLDPRT: open or insert them in SolidWorks and save as
   SLDPRT, or rebuild features from the Variables files.
2. The placeholder head's exact length could not be read from the .SLDPRT, so the heads are set
   to about 41-42 mm from the hub surface. Adjust "ProbeHead: Body Length" or
   "SwabHead: Body Length" to match.
3. The hub sockets are blind, so the tip wires (A: 3 wires, B: 3 wires) exit through the radial
   wire hole 8 mm from the hub and run along the hub face. Consider adding a wire slot to
   Hub_Turret.
4. Bristles, flock and tuft are simplified solids showing envelope only.
5. All dimensions are first-pass design values for a prototype.
