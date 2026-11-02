# ktpropulsion

KiCad 10 project for a Teensy 4.1, BMP180 module, and MPU6050 module with onboard logging.

Open `KTPropulsion.kicad_pro` in KiCad. Custom symbols, footprints, and the switch 3D model are stored in this repository and use project-relative library paths. Standard KiCad libraries are also required.

## Save a revision

Save the schematic and board in KiCad first, then run these commands in this folder:

```sh
git status
git add KTPropulsion.kicad_sch KTPropulsion.kicad_pcb KTPropulsion.kicad_pro libraries 3dmodels fp-lib-table sym-lib-table README.md .gitignore
git diff --cached --stat
git commit -m "Describe the design change"
```

Use `git log --oneline` to view checkpoints. Create an experiment branch with `git switch -c experiment-name`.

KiCad local state, automatic backups, routing experiments, and generated Gerber/DRC outputs are ignored. For fabrication, export fresh Gerbers and drills from a saved and checked revision; retain the ZIP with a Git release or separate archive. A commit records the design, not its fabrication approval.

Git history is local until a remote repository is configured and pushed. Close KiCad before restoring older design files to avoid overwriting them from an open editor.
