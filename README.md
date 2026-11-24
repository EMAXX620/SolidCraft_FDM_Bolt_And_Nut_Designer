FDM BOLT & NUT DESIGNER PLUGIN FOR SOLIDCRAFT
Version 3.1.0
======================================================================

<img width="1072" height="771" alt="image" src="https://github.com/user-attachments/assets/0153cea3-e4ba-47f8-b507-4a2e8757f7bd" />
<img width="705" height="465" alt="image" src="https://github.com/user-attachments/assets/dfcf7fc9-9e01-4053-ba40-a196cbc108db" />



3.1.0 requires 0.46.0 or later! Tested on 0.48.0
Buttons combined into one to save ribbon space!
<img width="393" height="829" alt="image" src="https://github.com/user-attachments/assets/82e92eae-b453-4c07-b6fd-65089ca61631" />


WHAT IT IS
----------
A companion to the FDM 90° Threads plugin. Instead of threading a shaft
you've already drawn, it makes whole bolts and nuts from scratch, as new
parts, ready to print:

  - The same FDM-friendly threads as FDM 90° Threads: 45° sides, wide
    flat tops and bottoms, and a clearance you choose. Its bolts and
    nuts fit each other, and nuts and holes made with FDM 90° Threads
    (or the Fusion 360 "FDM90" threads), when you use the same size and
    clearance.
  - A head of your choice, each with its own button:
      FDM Hex Bolt       - a hex head, for a wrench
      FDM Socket Bolt    - a round head with a hex key hole, like a socket
                       head cap screw
      FDM Phillips Bolt  - a round head with a Phillips cross (#0 to #4)
      FDM Torx Bolt      - a round head with a Torx (star) recess, or an
                           E-Torx head for an E socket
      FDM Slotted Bolt   - a round head with a slot for a flat screwdriver
    Each button's window only shows the settings for that head.
    (For a plain threaded rod, use FDM Rod in FDM 90° Threads.)
  - FDM Nut makes a hex nut, with its own button.
  - Round heads can be flat-topped or countersunk (a 90° cone that sits
    flush in a countersunk hole).
  - You set the head's size and thickness, or leave them empty and the
    plugin uses the standard (ISO) size for that thread.


WHAT YOU NEED
-------------
  - SolidCraft (the desktop version).
  - The file fdm-bolt-nut-designer.zip. This is the plugin. Don't unzip it;
    SolidCraft installs the zip directly.

You don't need FDM 90° Threads installed to use this plugin; they work
side by side.


HOW TO INSTALL
--------------
  1. Open SolidCraft.
  2. Go to Preferences > Plugins.
  3. Click "Install plugin..." and choose fdm-bolt-nut-designer.zip.
  4. Click Install.

Six new buttons appear on the ribbon in the "Plugins" group: FDM Hex
Bolt, FDM Socket Bolt, FDM Phillips Bolt, FDM Torx Bolt, FDM Slotted
Bolt and FDM Nut. They're also in the Plugins menu. All six have the
same plug icon, because SolidCraft doesn't let plugins choose their
own icons yet.

The settings windows don't show explanations when you hover over a
setting; this guide explains each one. (SolidCraft limits how big a
plugin's settings can be, and six windows only fit without them.)

Upgrading from FDM Bolt Designer (version 1.x): the plugin has a new
name, so first click Remove on "FDM Bolt Designer" in Preferences >
Plugins, then install fdm-bolt-nut-designer.zip. Otherwise SolidCraft
keeps both. Settings remembered in your designs carry over.

To update to a newer version of FDM Bolt & Nut Designer later: click
Remove on "FDM Bolt & Nut Designer", then install the new zip.


HOW TO USE IT
-------------
Click the button for the head you want. A window opens with that
head's settings and the thread settings; click Run. You don't need to
select anything first.

  Remember Settings/Use Last Settings
                Same as in FDM 90° Threads: tick it to reuse the
                settings from the last bolt this button made in this
                design. Each button remembers its own.

THE HEAD

  Head shape    FDM Socket, Phillips, Torx and Slotted Bolt
                (not E-TORX):
                  "cylinder"    - a flat-topped round head
                  "countersunk" - a 90° cone, for countersunk holes

  Head size (across flats)   (FDM Hex Bolt)
                The wrench size, for example 13 for a 13 mm wrench.
  Head diameter (FDM Socket, Phillips, Torx and Slotted Bolt)
                The round head's diameter. (For E-TORX, see below.)
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

  Style   (FDM Torx Bolt)
                  "TORX"   - a round head with a Torx (star) recess for
                             a T bit (the default)
                  "E-TORX" - the head itself is an external Torx
                             shape, for an E socket

  Torx size   (FDM Torx Bolt)
                "auto", or a size from the list. Sizes that go
                together are listed in pairs, such as "T25 / E5": the
                E5 socket fits the same shape as a T25 bit. TORX uses
                the T size, E-TORX the E size. T27, T45 and T90 are
                TORX only, and E14 is E-TORX only. (There's no E25:
                for a T25-size shape, the E size is E5.)
                "auto" for TORX picks the biggest T size that suits
                the Head diameter (for example T50 on an M10 socket
                head). "auto" for E-TORX uses the Head diameter if you
                give one (the biggest E size that fits within it),
                otherwise the usual E size for the thread (for
                example E10 for M8, E12 for M10). E24 is the biggest
                E size, which suits threads up to about M24.
                An E-TORX head is never countersunk, and is as tall as
                a hex head unless you set Head thickness.
                The Torx shape is made of real curved faces (each lobe
                and valley is a true cylinder), so it looks smooth in
                SolidCraft and prints smooth. It uses one sketch and
                about 13 steps, all in the bolt's timeline folder.

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

  Axis          The bolt starts at the origin of the design with its
                head and points along the axis. With Z (the default)
                it stands head-down on the floor of the design, the
                way you'd usually print it. It's named after the bolt,
                for example "FDM90-10x2 x 25 socket bolt". Move or
                rename it afterwards if you need to.

Things to know:
  - The bolt is made from ordinary SolidCraft steps (a cylinder,
    sketches, revolves, extrudes, a coil and a combine). They all go
    into one folder in the timeline, named after the bolt (for example
    "FDM90-10x2 x 20 socket bolt"), closed at first; click it to see
    the steps. Suppressing or deleting the folder does the same to the
    whole bolt. Undo removes all of it in one go.
  - Its sketches go into one group in the browser's Sketches folder,
    with the same name as the timeline folder. If SolidCraft won't
    make the group, the sketches stay where they are and a note says
    so; the bolt is made either way.
  - Its sketches are hidden when it's done, so you see just the part:
    the sketch group's eye in the browser is turned off. Only that
    bolt's or nut's sketches are hidden; click the group's eye to show
    them again.
  - The plugin doesn't update the bolt if you change something later.
    Delete its steps from the timeline and run it again.
  - Small threads (3 to 5 mm) are at the limit of FDM printing; see
    the FDM 90° Threads guide for printer settings.


FDM NUT
-------
Click FDM Nut. Like the bolt buttons, it needs nothing selected. The
nut lies flat on the floor of the design (with Axis Z), ready to print.

  Size, Pitch   The thread, as for bolts.

  Tolerance (clearance)
                The printing clearance. Use the same one as the bolt
                that goes in it.

  Thickness     How tall the nut is. Leave empty for the standard
                (ISO 4032) height, for example 8.4 mm for M10.

  Width across flats
                The wrench size. Leave empty for the standard size,
                for example 16 mm for M10.

  Chamfer inner A 45° countersink where the bolt threads in, on both
                faces, so the bolt starts easily from either side:
                  "auto"   - as deep as the thread (the default)
                  "custom" - the size in Chamfer inner size
                  "none"   - no countersink

  Chamfer outer A 45° bevel on the hex corners, on both faces:
                  "none"   - flat faces right out to the corners, the
                             best first layer for printing (the default)
                  "auto"   - like a standard nut's bevel
                  "custom" - the size in Chamfer outer size: how far
                             the bevel cuts in from the corners

  Hand, Axis, Remember Settings
                As for bolts. The nut's steps go into one timeline
                folder named after it, for example
                "FDM90-10x2 0.100e nut".


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

  "... is an E-TORX size only" / "... is a T (recess) size only"
      The Torx size you picked isn't in the series the Style uses.
      Pick a pair (like "T25 / E5"), or change the Style.

  "an E.. head is too small for a N mm thread"
  "E-TORX sizes go up to E24 ..."
      The E-Torx head would be narrower than the thread allows.
      Choose a bigger E size or "auto", or for big threads use
      FDM Hex Bolt or Style TORX.

  "... goes too far for this head"
      The Drive depth would leave too thin a floor, or break out
      through the side of a countersunk head. Make it shallower, or
      leave it empty.

  "a nut ... needs at least N mm across flats"
      The nut is too narrow to keep a wall around the thread. Make
      Width across flats bigger, or leave it empty.

  "the countersinks on the two faces would meet" / "the outer
  chamfers on the two faces would meet" / "... would cut into the
  thread" / "... reaches past the flats"
      A custom nut chamfer is too big for the nut. Make it smaller,
      use "auto", or make the nut thicker.

  "... has no N mm pitch; choose ..."
  "... goes up to a N mm clearance"
      As in FDM 90° Threads: pick one of the listed pitches, or a
      smaller clearance.


THE SOURCE CODE (fdm-bolt-nut-designer-source.zip)
--------------------------------------------------
You only need this to read or change how the plugin works. Like
FDM 90° Threads, it's a small C program compiled to WebAssembly that
sends SolidCraft the same commands you could run yourself. Its thread
code is copied unchanged from FDM 90° Threads (and its timeline
folders from version 1.6.0).

To rebuild: ./build.sh. It needs clang (with WebAssembly support),
wasm-ld and python3; README.md has the details and a list of the files,
including the tests, which run the plugin against a pretend SolidCraft
and draw the bolt or nut it would build.

