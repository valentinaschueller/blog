---
title: Zen and the Art of AUR Package Maintenance
description: ""
date: 2026-04-12
tags:
  - english
---

> Hi Florian,
> ich habe gesehen, dass Du verantwortlich für preCICE im Arch Linux User Repository bist. Brauchst Du Unterstützung für das Update auf preCICE v3?
>
> > Hallo Valentina,
> > Gegenfrage: Möchtest Du die Maintenance des AUR-Pakets übernehmen?

Through a weird sequence of events, I became the maintainer of [preCICE](https://precice.org) in the AUR.
This was two years ago: I had not done anything similar before, and I honestly had no idea what that would entail.
But I figured I would somehow be able to figure it out, said yes, and here we are!

Every time the preCICE team releases a new version, one of them (usually [Frédéric](https://github.com/fsimonis)) flags the package as out-of-date, and I get an e-mail.
Once that happens, I follow the same sequence of steps.
It is not hard, but still infrequent enough that I keep forgetting what to do exactly.
This might seem simple from the outside, but figuring out these steps was not trivial for me.[^1]
So, here is my standard operating procedure for upgrading preCICE in the AUR:

If you don't have it on your system yet:
1. Go to: https://aur.archlinux.org/packages/precice
2. Log in, clone package using ssh

Then:
1. `cd precice`.
2. Update the `PKGBUILD`: 
	1. Bump version number.
	2. Run `updpkgsums PKGBUILD`.
3. Delete `src/build` if it exists.
4. Run `makepkg` to make sure the package builds correctly.
5. Run tests: `ctest --test-dir src/build`.
6. Generate new `.SRCINFO`: `makepkg --printsrcinfo > .SRCINFO`.
7. Commit changes ("Bump version to...") and push.

> "Hier passiert keine Magic." ([Claudia Wagner](http://claudiawagner.info), 2017)

[^1]: It took me more than a year to learn about [`updpkgsums`](https://man.archlinux.org/man/updpkgsums.8.en)...
