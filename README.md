# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


/* Base Reset */
**css styling**
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
}

.container {
  display: grid;
  grid-template-areas:
    "header"
    "nav"
    "main"
    "footer";
  grid-template-columns: 1fr;
  grid-gap: 1rem;
  max-width: 1200px;
  margin: auto;
  padding: 1rem;
}

/* Grid Areas */
.header {
  grid-area: header;
  background: #333;
  color: #fff;
  padding: 1rem;
  text-align: center;
}

.nav {
  grid-area: nav;
  background: #444;
}

.nav ul {
  display: flex;
  justify-content: space-around;
  list-style: none;
  padding: 1rem;
}

.nav a {
  color: white;
  text-decoration: none;
}

.main {
  grid-area: main;
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 1rem;
}

.content {
  background: white;
  padding: 1rem;
}

.sidebar {
  background: #ddd;
  padding: 1rem;
}

.footer {
  grid-area: footer;
  background: #333;
  color: white;
  text-align: center;
  padding: 1rem;
}

/* Media Queries for Responsiveness */
@media (max-width: 768px) {
  .main {
    grid-template-columns: 1fr;
  }

  .nav ul {
    flex-direction: column;
    align-items: center;
  }
}

@media (max-width: 480px) {
  .header, .footer {
    font-size: 1rem;
  }

  .nav ul {
    font-size: 0.9rem;
  }
}
/* Base Reset */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
}

.container {
  display: grid;
  grid-template-areas:
    "header"
    "nav"
    "main"
    "footer";
  grid-template-columns: 1fr;
  grid-gap: 1rem;
  max-width: 1200px;
  margin: auto;
  padding: 1rem;
}

/* Grid Areas */
.header {
  grid-area: header;
  background: #333;
  color: #fff;
  padding: 1rem;
  text-align: center;
}

.nav {
  grid-area: nav;
  background: #444;
}

.nav ul {
  display: flex;
  justify-content: space-around;
  list-style: none;
  padding: 1rem;
}

.nav a {
  color: white;
  text-decoration: none;
}

.main {
  grid-area: main;
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 1rem;
}

.content {
  background: white;
  padding: 1rem;
}

.sidebar {
  background: #ddd;
  padding: 1rem;
}

.footer {
  grid-area: footer;
  background: #333;
  color: white;
  text-align: center;
  padding: 1rem;
}

/* Media Queries for Responsiveness */
@media (max-width: 768px) {
  .main {
    grid-template-columns: 1fr;
  }

  .nav ul {
    flex-direction: column;
    align-items: center;
  }
}

@media (max-width: 480px) {
  .header, .footer {
    font-size: 1rem;
  }

  .nav ul {
    font-size: 0.9rem;
  }
}
**the code**
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Flexbox & Grid Layout</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <div class="container">
    <header class="header">Responsive Header</header>
    <nav class="nav">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
    <main class="main">
      <section class="content">Main Content Area</section>
      <aside class="sidebar">Sidebar</aside>
    </main>
    <footer class="footer">Footer Info</footer>
  </div>
</body>
</html>

