# Birthday Website — Sheru ❤️

A cinematic, mobile-first birthday experience built with **HTML + CSS + vanilla JavaScript**.

## Run it

1. Extract the `birthday-sheru` folder.
2. Open the folder in VS Code.
3. Recommended: install/use the **Live Server** extension.
4. Right-click `index.html` → **Open with Live Server**.
5. Test on your phone using the same local network, or deploy the folder to a static host such as GitHub Pages / Netlify / Vercel.

> For a phone-accessible public link, upload the project to a static hosting service. No backend is required.

## Add the 12 photos

Put your files here:

```text
assets/images/photo1.jpg
assets/images/photo2.jpg
...
assets/images/photo12.jpg
```

The paths are already configured in `script.js`.

### Replace captions

Open `script.js` and edit only the `birthdayConfig` object near the top:

```javascript
photos: [
  { src: "assets/images/photo1.jpg", caption: "YOUR CAPTION" },
  ...
]
```

Do not rename the image files unless you also change the `src` values.

## Add the music

Place the audio file here:

```text
assets/music/her.mp3
```

The browser will **not autoplay the music before interaction**. It starts after Sheru presses **OPEN YOUR SURPRISE**.

Only use an audio file you are legally allowed to use/provide.

## Edit the quiz

Inside `birthdayConfig.quizQuestions`, each question looks like:

```javascript
{
  question: "Your question?",
  options: ["A", "B", "C", "D"],
  answer: 1,
  correct: "Message after a correct answer",
  wrong: "Message after a wrong answer"
}
```

`answer` is zero-based:
- `0` = first option
- `1` = second
- `2` = third
- `3` = fourth

You can add/remove questions.

## Edit compliments

Edit:

```javascript
compliments: [
  "Your message...",
  "Another message..."
]
```

## Edit Open When cards

Edit:

```javascript
openWhenMessages: [
  {
    title: "Open when you're sad 🥺",
    message: "Your personal message..."
  }
]
```

## Edit the secret reveal

Edit the `secretReveal` object if you want to change the setup, response, or punchline.

## Important personal-content rule

The project intentionally uses placeholders for photo captions and Open When messages where personal information was not provided. Replace those before sharing.

## File structure

```text
birthday-sheru/
├── index.html
├── style.css
├── script.js
├── README.md
└── assets/
    ├── music/
    │   └── her.mp3       ← add this
    └── images/
        ├── photo1.jpg   ← add these
        ├── photo2.jpg
        ├── ...
        └── photo12.jpg
```

## Features

- Cinematic loading screen
- Mystery intro
- User-triggered music
- Birthday reveal
- Story-style friendship section
- 12-photo editable configuration
- Click-to-expand photos
- 8-question editable quiz + score
- 30-second Catch the Hearts game
- Random compliment generator
- Open When cards
- Animated friendship score
- Suspense secret reveal
- Emotional finale + final car-showroom joke
- Replay without page reload
- Responsive mobile/desktop layouts
- Lazy image loading
- Keyboard-accessible controls
- `prefers-reduced-motion` support
- No external JS libraries required
