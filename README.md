# WORDZ KEYBOARD (v0.1 starter)

Native Android keyboard (InputMethodService) + Compose companion app.

## Build
Open in Android Studio (Hedgehog or newer, JDK 17). Let it sync; it creates the Gradle wrapper.
Or run `gradle wrapper` once, then `./gradlew assembleDebug`.
Versions used (AGP 8.5.2, Kotlin 1.9.24, Compose compiler 1.5.14, BOM 2024.06.00, compileSdk 34)
were NOT compiled in the authoring sandbox. Expect small first-build fixes.

## Done
- Real IME: QWERTY, shift/caps lock, symbols x2, numeric layout for number/phone fields,
  email/URI key variants, IME action key (Search/Go/Send/Next/Done), backspace repeat,
  long-press alternates, slide on space = cursor, long-press space = keyboard picker,
  auto-capitalisation, password fields detected.
- 8 themes, theme engine (data-driven), toolbar theme cycle.
- 9 animations + Off, allocation-free engine, reduced motion (also follows system animator scale).
- Clipboard history (pin, delete, search in app, filters, 2-tap clear in keyboard,
  confirm dialog in app, limit, pause), snippets (create/edit/delete/pin/insert), emoji panel.
- Compose app: setup status, themes, Animation Studio (uses the real KeyboardView), clipboard manager.
- No INTERNET permission.

## Not done yet (honest list)
- Custom photo theme, Liquid theme, remaining animations (glitch, electric, flip, wave, magnetic).
- Original sound profiles (currently the system key-click sound), haptic strength control.
- TalkBack per-key accessibility (needs ExploreByTouchHelper), landscape tuning, tests.
- Snippet shortcut expansion, emoji search, prediction. English only.
- Edge-to-edge insets for targetSdk 35. Real app icon. Room (JSON store used instead).
