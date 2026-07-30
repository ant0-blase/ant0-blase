# Anto B.

Reverse engineering, console preservation, and systems work on Linux and Windows.

I spend most of my time taking apart software that was never meant to be taken
apart — decompiling console games, reimplementing the hardware they ran on, and
writing the tooling needed to make that tractable. The rest goes to Linux and
Windows deployment automation.

---

## Featured work

### [MOHFrontline-PS2Recomp](https://github.com/ant0-blase/MOHFrontline-PS2Recomp)

A native PC port of **Medal of Honor: Frontline** (PlayStation 2) built by
*static recompilation* rather than emulation: the game's MIPS R5900 code is
translated ahead of time into C++, compiled into an ordinary executable, and run
against a hand-written implementation of the PS2 hardware it talks to.

The port boots cold, plays its intro, reaches the menus and loads a mission. The
hardware layer — VU0/VU1 microprogram interpreters, a software Graphics
Synthesizer, VIF1, the DMA tag walker and IOP HLE — is around 95 000 lines of
C++.

`C++` · `MIPS R5900` · `VU microcode` · `Graphics Synthesizer`

### [goldeneye-rag-decomp](https://github.com/ant0-blase/goldeneye-rag-decomp)

A byte-identical decompilation of **GoldenEye: Rogue Agent** (GameCube, `GOYE69`),
rebuilding the original binary exactly while progressively replacing assembly
with matching C/C++. Coverage is tracked against a real code-bytes metric rather
than a file count.

`PowerPC` · `C/C++` · `matching decompilation`

---

## What I work on

**Reverse engineering & preservation** — decompilation, static recompilation,
file-format research, hardware behaviour reimplementation. Both projects above
ship tooling only: they require a copy of the game you own.

**Linux** — Arch installation and tuning automation, VFIO/GPU passthrough on
muxless laptops, kernel builds, GNS3 lab provisioning.

**Windows deployment** — unattended installation, OOBE automation, WIM/VHD
imaging, BCD and boot repair, ISO preparation.

**Infrastructure** — CI/CD pipelines, containerised services, self-hosted
tooling.

---

## Notes on the repositories here

Most of what I publish is working tooling rather than finished products, and the
titles say so — several are explicitly marked work-in-progress. Anything that
touches a commercial game ships no game code and no assets: you supply your own
copy, and the tooling regenerates what it needs locally.
