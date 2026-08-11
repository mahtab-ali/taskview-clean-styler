# Submitting the Clean Task View theme

The Windhawk reviewer rejected the standalone mod because it uses XAML
Diagnostics, and Windows allows only **one** XAML Diagnostics consumer at a
time — so it would conflict with the popular *Windows 11 Taskbar Styler* mod.
Their recommended path is to ship this styling as a **theme** for that mod
instead. This folder contains exactly that.

## Test it locally first

1. Install **Windows 11 Taskbar Styler** from Windhawk.
2. Open its Settings → **Textual mode** and paste the contents of
   `CleanTaskView/styles.yaml`.
3. Save, press `Win+Tab`, and confirm each piece applies. If a selector
   doesn't match on your build, use the styler's element inspector to find the
   real type / `x:Name` and edit the target (see the README's "Tuning"
   section).

## Submit the theme (pull request)

The theme lives in a different repo from this mod:
<https://github.com/ramensoftware/windows-11-taskbar-styling-guide>

1. Fork that repo.
2. Copy the `CleanTaskView/` folder from here into the fork's `Themes/`
   folder, i.e. `Themes/CleanTaskView/` containing `README.md` and
   `screenshot.png`. (The styling-guide themes use a `README.md` per folder;
   `styles.yaml` here is just for convenient local pasting — the canonical
   styles live inside `README.md`.)
3. Add a row for **Clean Task View** to the theme table in the repo's
   top-level `README.md`, linking to `Themes/CleanTaskView/README.md` with the
   screenshot.
4. Open a pull request.

## What about the existing mod repo?

The standalone `task-desktop-view-styler.wh.cpp` mod can stay in this repo for
anyone who wants the standalone version, but it won't be accepted into the
Windhawk catalog as-is. Consider noting in the main README that the
recommended, catalog-friendly way to get this styling is the Clean Task View
theme above.
