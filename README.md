# 🎬 CineVault

> Your ultimate destination for movies & cinema — a full CRUD movie database app built with **Next.js 14 App Router**.

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## ✨ Features

- 🔍 **Search** movies by title, director, or genre
- 🏷️ **Filter** by genre (Action, Sci-Fi, Drama, Thriller, and more)
- 📊 **Sort** by Rating, Newest, Oldest, or A–Z
- 📄 **Pagination** — 4 movies per page
- ➕ **Add Movie** — dedicated page with full form validation
- ✏️ **Edit Movie** — dynamic route `/edit-movie/[id]`
- 🗑️ **Delete Movie** — remove from list instantly
- 🎥 **Movie Detail Page** — full page at `/movie-details/[id]`
- 🪟 **Quick-View Modal** — poster, cast, trailer link, synopsis
- 💾 **Session Persistence** — data stored in `sessionStorage`
- 🌑 **Cinematic Dark UI** — custom CSS with gold accents & animations

---

## 🖥️ Pages & Routes

| Route | Description |
|---|---|
| `/` | Home — movie grid with filter, search & pagination |
| `/add-movie` | Add a new movie |
| `/edit-movie/[id]` | Edit an existing movie |
| `/movie-details/[id]` | Full movie detail page |

---

## 🗂️ Project Structure

```
cinevault/
│
├── app/
│   ├── layout.js                  # Root layout (Bootstrap + globals)
│   ├── globals.css                # Base styles & pagination
│   ├── page.js                    # Home page
│   ├── add-movie/
│   │   └── page.js                # Add Movie page
│   ├── edit-movie/[id]/
│   │   └── page.js                # Edit Movie page
│   └── movie-details/[id]/
│       ├── page.js                # Movie Detail page
│       └── movie-details.css
│
├── Components/
│   ├── Header/                    # Navbar with search & Add Movie button
│   ├── FilterBar/                 # Hero section + genre filter + sort
│   ├── MovieCard/                 # Movie card with edit/delete/view actions
│   ├── MovieDetailModal/          # Quick-view popup modal
│   └── MovieForm/                 # Shared form (used by Add & Edit pages)
│
├── data/
│   └── movies.js                  # Default movie dataset (7 movies)
│
└── utils/
    ├── storageData.js             # sessionStorage get/set helpers
    └── constants.js               # Genres list & languages list
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| **Next.js 14** | App Router, dynamic routes, page navigation |
| **React 18** | UI components, hooks (`useState`, `useEffect`) |
| **React Bootstrap** | Form controls, layout grid, modal, badges |
| **React Icons** | FaEdit, FaTrash, FaSearch, FaPlus |
| **Custom CSS** | Cinematic dark theme, animations, hover effects |
| **sessionStorage** | Client-side data persistence (no backend needed) |

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Devarshiboghani/CINEVAULT-movie-app

# 2. Navigate into the project
cd movie-datatable

# 3. Install dependencies
npm install

# 4. Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📦 Dependencies

```bash
npm install next react react-dom
npm install react-bootstrap bootstrap
npm install react-icons
```

Make sure `bootstrap` CSS is imported in `app/layout.js`:

```js
import "bootstrap/dist/css/bootstrap.min.css";
```

---

## 🎬 Default Movies

The app comes pre-loaded with **7 movies** across multiple languages and genres:

| Title | Year | Genre | Rating |
|---|---|---|---|
| The Shawshank Redemption | 1994 | Drama | ⭐ 9.3 |
| The Dark Knight | 2008 | Action, Crime | ⭐ 9.0 |
| Inception | 2010 | Sci-Fi, Thriller | ⭐ 8.8 |
| Parasite | 2019 | Thriller, Drama | ⭐ 8.5 |
| Interstellar | 2014 | Sci-Fi, Adventure | ⭐ 8.6 |
| Avengers: Endgame | 2019 | Action, Sci-Fi | ⭐ 8.4 |
| 3 Idiots | 2009 | Comedy, Drama | ⭐ 8.4 |

---

## 💡 Key Implementation Notes

**Shared MovieForm Component**
Both `/add-movie` and `/edit-movie/[id]` use the same `MovieForm` component — `isEdit` prop controls the behavior and labels.

**Session Storage**
Movies are saved to `sessionStorage` on every add/edit/delete. On first load, default movie data is seeded if no session data exists.

**Dynamic Routing**
Next.js App Router handles `/movie-details/[id]` and `/edit-movie/[id]` — the `id` is matched against `sessionStorage` to find the correct movie.

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<p align="center">Made with ❤️ using Next.js</p>

## Demo Video
https://drive.google.com/file/d/1bSvMymT36-ZBgj23YRNy1A-imtNdfQU6/view?t=6.588g