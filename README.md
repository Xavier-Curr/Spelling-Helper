# Spelling Helper

A small, single-file web app that helps with spelling. Say a word out loud and it shows the word, breaks it into syllables, and reads it back. Built for a dyslexia-friendly, pop-up-window workflow alongside an essay document.

**Live version:** https://Xavier-Curr.github.io/spelling-helper/  

## Features

- **Speak a word:** uses the browser's built-in speech recognition (set to Australian English).
- **Syllable breakdown:** shows words like `beau · ti · ful`.
- **Read aloud:** click any word to hear it at a slower speed.
- **Word history:** keeps the last 5 words on screen for reference while typing.
- **Dyslexia-friendly design:** cream background, Verdana, generous letter spacing, high contrast, minimal clutter.

## How to use

1. Open the live link in **Chrome or Edge**.
2. Click **Tap & Say a Word** and allow the microphone when asked.
3. Say a word. Click it (or any word in the history) to hear it again.

**Tip:** to get a small standalone window, open the page in Chrome, then go to menu → *Cast, save, and share* → *Create shortcut…* and tick *Open as window*.

## Run it locally

No installs needed. Download `index.html` and open it in Chrome or Edge.
(Microphone permission is more reliable when the page is served over `https://` such as the live link above.)

## Known limitations

- **Syllable splitting is approximate.** It uses simple rules, not a dictionary, so some words will be wrong.
- **Needs internet for speech recognition.** Chrome and Edge send the audio to an online service to transcribe it, so avoid saying anything private.
- **Chrome / Edge only.** Firefox does not support the speech recognition feature.

## How it works

Everything lives in `index.html`:

| Part | Job |

| HTML - The page structure (mic button, word card, history) 
| CSS  - The look, with colours stored as variables in `:root` 
| JavaScript - Speech recognition, syllable splitting, read-aloud, history 

Browser features used: [Web Speech API](https://developer.mozilla.org/docs/Web/API/Web_Speech_API) (`SpeechRecognition` and `speechSynthesis`).

## Ideas for improvements (Subject to change)

- [ ] Skip duplicate words in the history
- [ ] "Clear history" button
- [ ] Slow / normal read-aloud speed toggle
- [ ] Better syllable accuracy (e.g. a small dictionary for common tricky words)

## License

MIT. See [LICENSE](LICENSE).
