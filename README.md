<div align="center">

# 🎬 WebFlyx

**A curated collection of movie titles, classic films, and memorable quotes, tracked with Git.**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)
![CSV](https://img.shields.io/badge/Data-CSV-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/status-active-brightgreen?style=for-the-badge)

</div>

---

## 📖 Overview

**WebFlyx** is a small, content-only repository holding a movie catalog: a list of titles, a dataset of classic films, and a library of well-known movie quotes.

I built it mainly to practice **real-world Git workflows** in a hands-on way, including:

- Making atomic, well-labelled commits
- Creating and working on **feature branches**
- **Merging** branches back into `main`, including true merge commits
- Syncing with a **remote** (`origin`) and resolving divergent histories
- Keeping a clean, readable project history

## 📂 Repository Structure

```text
webflyx/
├── contents.md        # Index describing each file in the collection
├── titles.md          # Movie titles in the WebFlyx collection
├── classics.csv       # Classic movies dataset (title, director, year)
└── quotes/
    ├── dune.md        # Memorable quotes from Dune
    └── starwars.md    # Memorable quotes from Star Wars
```

## 🗂️ Content

### 🎞️ Titles (`titles.md`)

| # | Title |
|---|-------|
| 1 | A River Runs Through It |
| 2 | Fight Club |
| 3 | 12 Years a Slave |
| 4 | The Big Short |
| 5 | 12 Monkeys |
| 6 | The Curious Case of Benjamin Button |

### 🏆 Classics (`classics.csv`)

A comma-separated dataset with the schema `title, director, year`:

| Title | Director | Year |
|-------|----------|:----:|
| Monty Python and the Holy Grail | Terry Gilliam | 1975 |
| The Goonies | Richard Donner | 1985 |
| The Breakfast Club | John Hughes | 1985 |
| One Crazy Summer | Savage Steve Holland | 1986 |
| The Princess Bride | Rob Reiner | 1987 |
| Willow | Ron Howard | 1988 |

### 💬 Quotes (`quotes/`)

| File | Movie | Quotes |
|------|-------|:------:|
| [`dune.md`](quotes/dune.md) | *Dune* | 2 |
| [`starwars.md`](quotes/starwars.md) | *Star Wars* | 5 |

## 🌿 Git Workflow

Commits carry a letter prefix (`A:`, `B:`, `C:` …) so the history reads in order and each step is easy to find in `git log`.

```text
* L: add Psycho                      (add_classics)
*   K: merge origin/main             (main)
|\
| * J: update classics.csv
|/
*   Merge branch 'update_dune'
|\
| * I: add fear quote
| * H: add spice quote
* | I: add fear quote
* | H: add spice quote
|/
* G: update titles
*   F: Merge branch 'add_classics'
|\
| * D: add classics
* | E: update contents
|/
* C: add quotes
* B: second commit
* A: add contents.md
```

| Branch | Purpose |
|--------|---------|
| `main` | Stable, up-to-date collection |
| `add_classics` | Introduced the `classics.csv` dataset; now one commit ahead of `main` (adds *Psycho*, 1960) |
| `update_dune` | Added new *Dune* quotes (merged into `main`) |

To see the full graph yourself:

```bash
git log --oneline --graph --all
```

## 🚀 Getting Started

Clone the repository:

```bash
git clone https://github.com/QaisRjoob/webflyx.git
```

```bash
cd webflyx
```

Browse the collection:

```bash
cat titles.md
```

```bash
column -s, -t < classics.csv
```

## 🤝 Contributing

Contributions are welcome. To add a movie, a classic, or a quote:

1. **Fork** the repository.
2. Create a feature branch: `git checkout -b add_<something>`
3. Make your changes, following the existing format:
   - `titles.md` → one Markdown bullet per title
   - `classics.csv` → one row per film: `title, director, year`
   - `quotes/<movie>.md` → one quoted bullet per line
4. Commit with a clear message: `git commit -m "add <something>"`
5. Push and open a **Pull Request**.

If you add a new file, please also list it in [`contents.md`](contents.md).

## 👤 Author

**Qais Rjoob**

[![GitHub](https://img.shields.io/badge/GitHub-QaisRjoob-181717?style=flat&logo=github)](https://github.com/QaisRjoob)

---

<div align="center">

⭐ If you found this repository useful, consider giving it a star!

</div>
