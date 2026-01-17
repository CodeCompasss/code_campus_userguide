

## Clipboard (Copy & Paste in Linux)

Copy and paste may feel **surprisingly confusing at first on Linux**, especially if you are coming from **macOS or Windows**, where the same shortcuts work everywhere.

On Linux, the confusion mainly comes from the **terminal**.

---

## Why Ctrl + C / Ctrl + V Don’t Work in the Terminal

In graphical apps (like browsers or editors), copy and paste work normally:

* **Copy:** `Ctrl + C`
* **Paste:** `Ctrl + V`

But in the **terminal**, these keys already have special meanings:

* `Ctrl + C` → **Stops (kills) a running command**
* `Ctrl + V` → **Inserts a control character**

So Linux uses **different shortcuts** inside the terminal.

---

## Terminal Copy & Paste Shortcuts

Inside the terminal, use:

* **Copy:** `Shift + Ctrl + C`
* **Paste:** `Shift + Ctrl + V`

If you accidentally press `Ctrl + V`, you may see a strange character appear.
Just **delete it** and use the correct paste shortcut.

💡 Tip:
This takes some time to build muscle memory — everyone struggles with it at first.

---

## Copying Text with the Mouse (Terminal & Zellij)

When using terminal tools like **Zellij**, copying with the mouse has extra rules:

1. **Hold `Shift`**
2. **Select text with the mouse**
3. Press **`Shift + Ctrl + C`** to copy

Without holding `Shift`, your mouse selection may not work correctly.

⚠️ Note:
Mouse selection can feel a bit **finicky** at first, especially with exact positioning — this is normal. You’ll get used to it quickly.

---

## Clipboard Extension (Visual Clipboard History)

Codekub also includes a **clipboard extension** in the **bottom bar**.

This allows you to:

* See **everything you’ve copied recently**
* Quickly reuse previous text
* Avoid losing important copied commands or code

It’s extremely useful when:

* Copying multiple commands
* Switching between documentation and terminal
* Learning Linux and experimenting

Think of it as a **clipboard history manager** that makes learning much easier.

