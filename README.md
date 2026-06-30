# My android keyboard layout.

This is a hack-ish construction of a custom keyboard layout for me. I
have some peculiarities:

- capslock and backspace swapped
- left control and left alt switched
- Numbers in the order 7531902468 ("dvorak classic" order, but with
  standard english-layout symbols when shifted)
- Right alt + querty key below gives left handed shortcuts:
  - "e" -> up
  - "s" -> left
  - "d" -> down
  - "f" -> right
  - "a" -> delete
  - "q" -> page up
  - "z" -> page down
  - "r" -> '{' (']' if shifted)
  - "r" -> '}' (']' if shifted)
  - "g" -> '\'
  - For these, I had to adjust the modifier keys to change the "action
    key" to "alt" in the physical keyboard settings.  Otherwise the
    action key would override these shortcuts, and the "ralt" key
    wasn't what I expected.

For security I made a new project and manually set it up, so that I
wasn't using someone else's compiled code.

The following things were very helpful, since I don't know app
development (really, this was a struggle to figure out):
- https://ris58h.github.io/exkeymo/simple.html
- https://github.com/ris58h/custom-keyboard-layout
- https://codebenchers.com/blog/android-keyboard-remapping-arrow-keys-kcm
  (the 'replace' keyword in the .kcm file)
