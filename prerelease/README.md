# Compact Toolchain Prereleases

This directory contains prerelease versions of the Compact toolchain, which
includes the Compact compiler.  These are versions that are publicly available
but not yet ready to install via the Compact devtools (the `compact`
command-line tool).

**Prerelease versions are intended for users who really, really need to test an
about-to-be-released version of the toolchain.**  If you are not such a user,
you should stick to officially released (and supported) versions that can be
installed via the devtools.

## Versions

Prerelease binaries are in directories corresponding to releases.  For example,
you will find prerelease binaries for Compact toolchain 0.27 in the directory
`compactc-0.27`.  The binaries have version numbers ending with `-rc.x`
("release candidate", where _x_ is the release candidate number).

Binaries are provided for x86-64 Linux, Apple silicon (aarch64) macOS (darwin),
and x86-64 macOS (darwin).

## Installation Instructions

To install a prerelese version, follow the manual installation process:

1. Download the `.zip` file for your architecture and OS.

1. Unzip them into a directory of your choice

The toolchain consists of multiple binaries (`format-compact` is the formatter,
`fixup-compact` is the fixup tool, `zkir` is used by the compiler to generate
prover and verifier keys, `compactc.bin` is the compiler binary but you should
invoke this via the shell script `compact`).

**IMPORTANT:** On macOS these binaries are not signed so the OS will initially
block them from running.  When you see a dialog box about them, choose "Done"
(do not move them to the trash).  Then open the "Privacy & Security" System
Settings.  Scroll down to the bottom of the settings and you will see, for
example, `"format-compact" was blocked to protect your Mac.`.  Click "Allow
Anyway".

You will have to do this for each binary (note that the compiler binary
automatically invokes the `zkir` binary if it needs to generate keys).
