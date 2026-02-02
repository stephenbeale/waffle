# Waffle - Product Roadmap

## Feature 1: No-Colour-Fill Button Toggle ✅

Add a toggle that removes the colour background from buttons, leaving only the text label. This forces players to read the word on each button rather than relying on the button colour as a visual cue.

## Feature 2: Difficulty Levels (Easy / Medium / Hard) ✅

Replace individual toggles with three preset difficulty levels that group settings together.

### Easy

- Colour-filled buttons (background matches label)
- Labels shown on buttons
- No button shuffling
- 10-second starting timer
- Timer reduces by 1s every 10 correct answers (minimum 2s)
- Level "complete" at 100 correct answers (but user can continue for high scores)

### Medium

- Colour-filled buttons
- Labels hidden
- Shuffle buttons every 10 answers
- 8-second starting timer
- Timer reduces by 1s every 10 correct answers (minimum 2s)
- Level "complete" at 100 correct answers (but user can continue for high scores)

### Hard

- No colour fill on buttons (plain/neutral background)
- Labels shown (text only, no colour cue)
- Shuffle button order after every correct answer
- 6-second starting timer
- Timer reduces by 1s every 10 correct answers (minimum 1s)
- Level "complete" at 100 correct answers (but user can continue for high scores)

### Custom (optional)

- Allow manual toggle configuration for players who want to mix and match settings outside the presets

## Feature 3: UI Improvements ✅

- Left-align toggle options on the start screen for visual clarity

## Feature 4: Audio Response Mode ✅

Add a mode where the player's microphone is the only input method. The player must say the colour name out loud instead of clicking a button. Uses the Web Speech Recognition API to capture and evaluate spoken answers in real time.

### Considerations

- Browser support (Web Speech API is primarily Chrome/Edge)
- Microphone permission handling and clear UI feedback
- Tolerance for accent/pronunciation variation
- Visual feedback when speech is detected vs recognised
- Fallback or error messaging for unsupported browsers
- May need a short cooldown between rounds to avoid picking up residual audio

## Feature 5: Extra Colours ✅

Add option to increase the number of colours from 5 up to 10 in Custom mode. Additional colours: orange, pink, purple, cyan, brown.

## Feature 6: Language Selection ✅

Add a toggle or dropdown to switch the game language. Colour words and button labels will display in the selected language, adding an extra cognitive challenge for multilingual players or language learners.

## Feature 7: Increasing difficulty levels ✅

Add a fractional time reduction after user hits the minimum time limit - reduce down by 0.2 seconds each 10 correct answers, making it eventually impossible. At 0.2 seconds, after 10, tell the user they win - only way to improve is by improving response time.

## Feature 8: Leaderboard ✅

Ask user to input their name for leaderboard, to compete against themselves at this point. Tell them if they performed a personal best after subsequent runs, or what their goal is if not.

## Feature 9: Use different colours to Cyan ✅

Use brown instead of cyan. (Brown is used in the extended colour set; cyan was never included.)

### Supported Languages

- English (default)
- Welsh (Cymraeg)
- Italian (Italiano)
- Spanish (Español)
- French (Français)
- German (Deutsch)

### Colour Translations

| English | Welsh | Italian | Spanish | French | German |
|---------|-------|---------|---------|--------|--------|
| Red | Coch | Rosso | Rojo | Rouge | Rot |
| Green | Gwyrdd | Verde | Verde | Vert | Grün |
| Blue | Glas | Blu | Azul | Bleu | Blau |
| Grey | Llwyd | Grigio | Gris | Gris | Grau |
| Yellow | Melyn | Giallo | Amarillo | Jaune | Gelb |

### Considerations

- Language selector on start screen (dropdown or button group)
- Persist language choice in localStorage
- Update voice recognition language code when using audio mode (e.g., `es-ES`, `fr-FR`)
- Consider adding voice aliases for each language to handle pronunciation variations
