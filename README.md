# Imposter

A pass-the-phone party word game. Everyone gets the same secret word except one
player, who sees only the word IMPOSTER and the category. Play it at
[mtw4244.work/imposter](https://mtw4244.work/imposter).

No build step, no dependencies, no network calls. Three files of plain HTML,
CSS and JavaScript, so opening `index.html` in a browser is enough.

## How to play

1. Pick a player count (3 to 20) and a category, then hand the phone around.
2. Each player taps Show word, looks, and taps Next player before passing it on.
   The word re-blurs itself every time, so nobody sees the previous card.
3. Everyone gets the same secret word, except the imposter, who gets the
   category only.
4. Go round the circle. Each player says one clue about the word. The imposter
   has to bluff something that fits the category without knowing the word.
5. Vote on who the imposter is. Civilians win if they get it right. The imposter
   wins by surviving the vote, or by guessing the secret word.

## Categories

Animals, Food and drink, Famous people, Places, Movies and TV, Sport, Around the
house, Jobs, Music, Nature and weather, plus a Surprise me option that picks a
category at random. 25 words each.

To add your own, edit the `CATEGORIES` array near the top of the script block in
`index.html`. Each entry is `{ id, name, words: [...] }` and nothing else needs
changing, the category buttons are generated from that array.

## Running it

Open `index.html` directly, or serve the folder:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole game, markup and logic |
| `style.css` | Shared stylesheet from mtw4244.work |
| `theme.js` | Theme picker, 21 editor colour schemes, saved in `localStorage` |

## Licence

MIT, see [LICENSE](LICENSE).
