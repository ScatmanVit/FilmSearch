<div align="center">

# FilmSearch

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

</div>

---

A client-side movie search bar. No backend, no dependencies — just DOM manipulation and a `formatString` function doing more work than it looks like.

The interesting detail: search is normalized before comparison. Accents are stripped, case is ignored, whitespace is trimmed. So `"Dirty Dancing"`, `"dirty dancing"`, and `"dírty dáncing"` all hit the same result. That one function is the whole engine.

---

## What's under the hood

- Live filtering on every keystroke via `input` event
- `normalize('NFD')` + regex strips accents before comparison — search works regardless of how the user types
- Items are shown/hidden with `display` toggling, no re-renders
- "No results" message appears only when every item is hidden
- Custom scrollbar styled for both Webkit and Firefox
- Single JS file, zero dependencies

---

## Running locally

```bash
git clone https://github.com/ScatmanVit/FilmSearch.git
```

Open `src/html.html` in your browser or use Live Server in VSCode.
