# My android keyboard layout.

This is a hack-ish construction of a custom Android physical keyboard
layout for me.  This is *not* an on-screen keyboard layout (that's
normal Dvorak).  If you connect a bluetooth/wired keyboard, and you
search "physical keyboard" in the settings, you can go there and set
specific layouts for the physical keyboard.  Dig around and you'll
find it.  This setting allows me to use all the custom things I have
set up below.

The keyboard layout is `English (US), Dvorak rkdarst` on the list.

I have some peculiarities to my layout.  It is like a Dvorak layout,
but:

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
  - **Setup:** For these, I had to adjust the modifier keys (within
    the physical keyboard settings) to change the "action key" to
    "Alt".  Otherwise right alt is some action key that does some
    other Android hotkey stuff.  would key did some other Android
    hotkey stuff.


Tuples of (keycode, original key, what I want it to be) - keycodes
from ExKeyMo web:
- (29, CTRL_LEFT, ALT_LEFT)
- (56, ALT_LEFT, CTRL_LEFT)
- (126, META_RIGHT)
- (100, ALT_RIGHT)
- (97 CTRL_RIGHT)
- (125, META_LEFT)  (windows)
- (126, META_RIGHT)  (command/mac-option)
- (464, FUNCTION)


For security I made a new project and manually set it up, so that I
wasn't using someone else's compiled code.

The following things were very helpful, since I don't know app
development (really, this was a struggle to figure out):
- https://ris58h.github.io/exkeymo/simple.html
- https://github.com/ris58h/custom-keyboard-layout
- https://codebenchers.com/blog/android-keyboard-remapping-arrow-keys-kcm
  (the 'replace' keyword in the .kcm file)
- [Generic.kl](https://android.googlesource.com/platform/frameworks/base/+/master/data/keyboards/Generic.kl)
- [Generic.kcm](https://android.googlesource.com/platform/frameworks/base/+/master/data/keyboards/Generic.kcm)


Version history:

- 3: fix what appears to be a bug with the left control definitions.
  The "new" LCtrl (physical LAlt button) doesn't seem to be working here.
