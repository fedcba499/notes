## LibPkg
It stands for Library Package Project. It’s not a symbol or footprint itself — it’s a container that holds:
- One or more schematic library files (.SchLib)
- One or more PCB footprint library files (.PcbLib)
- Optional 3D models (.Step files)

Links between them. The .LibPkg keeps these all organized so you can compile them into a single **.IntLib** (Integrated Library)
> Using SnapEDA we can download .IntLib and use it in Altium projects

> Using an .IntLib in Altium is the “ready-to-eat” version of a library, so we don’t have to deal with linking symbols and footprints.

> Inside, .LibPkg (which contains schmatics, pcb and 3d Step files), we can edit schematic symbols (.SchLib) and PCB footprints (.PcbLib).
We can link schematic symbols to footprints in the Library Package editor. When linking is completed, we can compile the .LibPkg to produces a .IntLib file.

