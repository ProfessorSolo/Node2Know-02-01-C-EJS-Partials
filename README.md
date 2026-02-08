# Node2Know — EJS Partials

A demonstration of modularizing EJS templates using Partials.

This demo refactors the previous examples by extracting common UI elements (Header, Footer) into reusable partial files.

Core concepts:

- Creating partial views (`views/partials/`)
- Using `<%- include() %>` to inject partials
- Passing data to partials (e.g., custom titles)
- DRY (Don't Repeat Yourself) principles in view templates

Example:

```html
<!-- views/index.ejs -->
<%- include("partials/header", { title: "Home Page" }) %>

<main>
  <h1>Welcome</h1>
</main>

<%- include("partials/footer") %>
```

---

## ✅ Prereqs

- **Node.js**
- **npm**

Check:

```bash
node -v
npm -v
```

---

## 📦 Install

```bash
npm install
```

---

## ▶️ Run

```bash
npm run dev
```

---

## 🧪 Try it

### Home Page

Open:

- `http://localhost:3000/`

Notice the header and footer are present, but their code is not in `index.ejs`.

### Things Page

Open:

- `http://localhost:3000/things`

The same header and footer are reused here, maintaining consistency across the site.

---

## 🧠 Key Code

### The Partial (`header.ejs`)

```html
<!-- views/partials/header.ejs -->
<header>
  <nav>...</nav>
  <h1><%= title %></h1>
</header>
```

### Including It

```html
<!-- views/index.ejs -->
<!-- Pass a custom 'title' variable to the partial -->
<%- include("partials/header", { title: "// EJS Partials" }) %>
```

---

## 📁 Project Structure

```txt
.
├── app.js
├── views/
│   ├── index.ejs        # Uses partials
│   ├── things.ejs       # Uses partials
│   └── partials/        # Reusable components
│       ├── header.ejs
│       └── footer.ejs
├── public/
└── README.md
```

---

## Repo

- https://github.com/ProfessorSolo/Node2Know-02-01-C-EJS-Partials.git

---

## License

**Node2Know-LEARN-1.0**
