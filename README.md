# SolidCraft_FDM_Bolt_Designer
Create 3D printable bolts with a variety of head types and sizes.


FDM BOLT DESIGNER PLUGIN FOR SOLIDCRAFT
Version 1.4.0
======================================================================

<img width="886" height="763" alt="image" src="https://github.com/user-attachments/assets/9c2964e3-3c74-4d17-b3a5-92324e0dc3ef" />


WHAT IT IS
----------
A companion to the FDM 90° Threads plugin. Instead of threading a shaft
you've already drawn, it makes a whole bolt from scratch, as a new part,
ready to print:

  - The same FDM-friendly threads as FDM 90° Threads: 45° sides, wide
    flat tops and bottoms, and a clearance you choose. Bolts from this
    plugin screw into nuts and holes made with FDM 90° Threads (or the
    Fusion 360 "FDM90" threads) when you use the same size and clearance.
  - A head of your choice, each with its own button:
      FDM Hex Bolt       - a hex head, for a wrench
      FDM Socket Bolt    - a round head with a hex key hole, like a socket
                       head cap screw
      FDM Phillips Bolt  - a round head with a Phillips cross (#0 to #4)
      FDM Slotted Bolt   - a round head with a slot for a flat screwdriver
    Each button's window only shows the settings for that head.
    (For a plain threaded rod, use FDM Rod in FDM 90° Threads.)
  - Round heads can be flat-topped or countersunk (a 90° cone that sits
    flush in a countersunk hole).
  - You set the head's size and thickness, or leave them empty and the
    plugin uses the standard (ISO) size for that thread.


WHAT YOU NEED
-------------
  - SolidCraft (the desktop version).
  - The file fdm-bolt-designer.zip. This is the plugin. Don't unzip it;
    SolidCraft installs the zip directly.

You don't need FDM 90° Threads installed to use this plugin; they work
side by side.


HOW TO INSTALL
--------------
  1. Open SolidCraft.
  2. Go to Preferences > Plugins.
  3. Click "Install plugin..." and choose fdm-bolt-designer.zip.
  4. Click Install.

Four new buttons appear on the ribbon in the "Plugins" group: FDM Hex Bolt,
FDM Socket Bolt, FDM Phillips Bolt and FDM Slotted Bolt. They're also in the
Plugins menu. All four have the same plug icon, because SolidCraft
doesn't let plugins choose their own icons yet.

To update from an earlier version: in Preferences > Plugins, click Remove on
"FDM Bolt Designer", then install the new zip.


HOW TO USE IT
-------------
Click the button for the head you want. A window opens with that
head's settings and the thread settings; click Run. You don't need to
select anything first.

  Remember Settings/Use Last Settings
                Same as in FDM 90° Threads: tick it to reuse the
                settings from the last bolt this button made in this
                design. Each button remembers its own. Where the bolt
                goes and its name are never reused.

THE HEAD

  Head shape    FDM Socket, Phillips and Slotted Bolt:
                  "cylinder"    - a flat-topped round head
                  "countersunk" - a 90° cone, for countersunk holes

  Head size (across flats)   (FDM Hex Bolt)
                The wrench size, for example 13 for a 13 mm wrench.
  Head diameter (FDM Socket, Phillips and Slotted Bolt)
                The round head's diameter.
                Leave empty for the standard size.

  Head thickness
                How tall the head is, for example 4 mm or 8 mm.
                Leave empty for the standard thickness.
                A countersunk head has to be at least as thick as its
                cone; the plugin tells you the minimum if it's too thin.

  Flat head top (easier to print)   (FDM Hex Bolt, ticked by default)
                Keeps the top of the hex head a flat hexagon, so the
                whole head sits on the print bed for a good first layer.
                Untick it for the 30° bevel real hex bolts have on top.

  Chamfer head top   (round heads)
                Bevels the top edge of a flat-topped round head
                slightly.

THE DRIVE (each round-head button shows its own)

  Hex socket size   (FDM Socket Bolt)
                The hex key the socket fits: "auto" picks the standard
                one for the thread, or choose a size (metric 1.5 to 27
                mm, or inch 1/16 to 5/8 in).

  Phillips size (FDM Phillips Bolt) "auto", or #0, #1, #2, #3, #4.

  Slot (screwdriver blade)   (FDM Slotted Bolt)
                "auto", or a screwdriver blade as thickness x width,
                for example 1 x 5.5 mm. The slot is as wide as the
                blade is thick and as long as the blade is wide, plus
                the Drive clearance all round (so 1 x 5.5 mm gives a
                slot 1.3 mm wide and 5.8 mm long). "auto" uses the
                standard slot for the thread, or a smaller blade if
                that won't fit the head.

  Full-width slot   (FDM Slotted Bolt, unticked by default)
                Tick it to run the slot right across the head, like
                a classic slotted screw.

  Drive depth   How deep the socket, cross or slot goes. Leave empty
                for a sensible depth.

  Drive clearance
                Extra room on every side of the socket, cross or slot,
                so the printed hole takes the tool. 0.15 mm is a good
                start; make it bigger if the key or screwdriver is
                tight, smaller if it's loose.

  If the head is too small for the standard drive, "auto" picks a
  smaller one and says so. If you choose a size yourself and it doesn't
  fit, the plugin tells you what does.

THE THREAD

  Diameter, Pitch, Clearance class, Hand
                The same as in FDM 90° Threads, for sizes 3 mm to 60 mm.
                The diameter list shows each size with its pitches, for
                example "20 (2, 3, 4)" is 20 mm with pitch 2, 3 or 4.
                Use the same clearance as the nut or threaded hole the
                bolt goes into.

  Thread length The length of the threaded part.

  Plain shank length
                An unthreaded part between the head and the thread.
                0 threads the bolt right up to the head.

  Tip chamfer   A 45° bevel on the end, so it starts into the nut
                easily. "auto" (as deep as the thread), "custom" (the
                size in Chamfer size) or "none".

WHERE IT GOES

  Axis, Base X / Y / Z
                The bolt starts at the base point with its head and
                points along the axis. With Z (the default) it stands
                head-down on the floor of the design, the way you'd
                usually print it.

  Body name     Optional. Otherwise it's named after the bolt, for
                example "FDM90-10x2 x 25 socket bolt".

Things to know:
  - The bolt is made from ordinary SolidCraft steps (a cylinder,
    sketches, revolves, extrudes, a coil and a combine). They all go
    into one folder in the timeline, named after the bolt (for example
    "FDM90-10x2 x 20 socket bolt"), closed at first; click it to see
    the steps. Suppressing or deleting the folder does the same to the
    whole bolt. Undo removes all of it in one go.
  - The plugin doesn't update the bolt if you change something later.
    Delete its steps from the timeline and run it again.
  - Small threads (3 to 5 mm) are at the limit of FDM printing; see
    the FDM 90° Threads guide for printer settings.


IF SOMETHING GOES WRONG
-----------------------
  "... must be at least N mm across flats" / "... at least N mm across"
      The head is smaller than the thread. Make Head size bigger, or
      leave it empty.

  "... needs at least N mm thickness for its 90° cone"
      A countersunk head that wide needs to be at least that thick.
      Make it thicker or narrower, or leave both empty.

  "... doesn't fit a N mm head"
      The hex key, Phillips size or slot you chose is too big for the
      head. Choose a smaller one, use "auto", or make the head bigger.
      For a slot, ticking Full-width slot also works.

  "... goes too far for this head"
      The Drive depth would leave too thin a floor, or break out
      through the side of a countersunk head. Make it shallower, or
      leave it empty.

  "... has no N mm pitch; choose ..."
  "... goes up to a N mm clearance"
      As in FDM 90° Threads: pick one of the listed pitches, or a
      smaller clearance.


THE SOURCE CODE (fdm-bolt-designer-source.zip)
----------------------------------------------
You only need this to read or change how the plugin works. Like
FDM 90° Threads, it's a small C program compiled to WebAssembly that
sends SolidCraft the same commands you could run yourself. Its thread
code is copied unchanged from FDM 90° Threads 1.5.2.

To rebuild: ./build.sh. It needs clang (with WebAssembly support),
wasm-ld and python3; README.md has the details and a list of the files,
including the tests, which run the plugin against a pretend SolidCraft
and draw the bolt it would build.
