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

html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with Flexbox</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- Navigation Bar -->
  <nav class="navbar">
    <ul class="nav-list">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Content -->
  <div class="container">
    <header>
      <h1>Welcome to Our Website</h1>
      <p>This is a responsive page layout example using Flexbox and Media Queries.</p>
    </header>

    <section class="content">
      <div class="card">
        <h2>Feature 1</h2>
        <p>Description of feature 1.</p>
      </div>
      <div class="card">
        <h2>Feature 2</h2>
        <p>Description of feature 2.</p>
      </div>
      <div class="card">
        <h2>Feature 3</h2>
        <p>Description of feature 3.</p>
      </div>
    </section>
  </div>

</body>
</html>

CSS
/* General Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
}

/* Navbar Styles */
.navbar {
  background-color: #333;
}

.nav-list {
  display: flex;
  justify-content: space-around;
  padding: 10px;
  list-style: none;
}

.nav-list li {
  margin: 0 15px;
}

.nav-list a {
  color: white;
  text-decoration: none;
  font-size: 16px;
  padding: 10px 20px;
}

.nav-list a:hover {
  background-color: #555;
  border-radius: 5px;
}

/* Main Container */
.container {
  display: flex;
  flex-direction: column;
  padding: 20px;
  max-width: 1200px;
  margin: auto;
}

/* Header */
header {
  text-align: center;
  margin-bottom: 20px;
}

header h1 {
  font-size: 2rem;
  color: #333;
}

/* Content Section */
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  gap: 20px;
}

.card {
  background-color: white;
  border: 1px solid #ddd;
  padding: 20px;
  width: 30%;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  text-align: center;
}

.card h2 {
  color: #333;
  font-size: 1.5rem;
}

/* Media Queries */

/* Mobile (up to 600px) */
@media (max-width: 600px) {
  .nav-list {
    flex-direction: column;
    align-items: center;
  }

  .container {
    padding: 10px;
  }

  .content {
    flex-direction: column;
    align-items: center;
  }

  .card {
    width: 80%;
    margin-bottom: 20px;
  }
}

/* Tablet (600px to 1024px) */
@media (max-width: 1024px) {
  .content {
    flex-direction: row;
    justify-content: space-between;
  }

  .card {
    width: 45%;
  }
}

/* Desktop (1024px and above) */
@media (min-width: 1024px) {
  .card {
    width: 30%;
  }
}
