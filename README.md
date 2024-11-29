# Professional Resume Website

A professional resume website template built with Flask and Bootstrap, featuring Introduction, Skills, Experience, Education, Portfolio, and Blog sections. The website implements a modern, responsive design with dark mode support and smooth animations.

## Features

- **Responsive Design**: Mobile-first approach using Bootstrap 5
- **Dark Mode**: Toggle between light and dark themes with persistent settings
- **Smooth Animations**: CSS transitions and scroll animations
- **Dynamic Blog**: SQLite-powered blog section with Flask-SQLAlchemy
- **Portfolio Showcase**: Project cards highlighting various applications
- **Section Navigation**: Smooth scrolling with active state tracking

## Tech Stack

- **Backend**:
  - Flask
  - Flask-SQLAlchemy
  - Flask-Migrate
  - SQLite

- **Frontend**:
  - Bootstrap 5
  - Font Awesome 6
  - Custom CSS with CSS Variables
  - Vanilla JavaScript

## Prerequisites

- Python 3.11 or higher
- pip (Python package installer)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd resume-website
```

2. Install dependencies:
```bash
pip install flask flask-sqlalchemy flask-migrate
```

3. Initialize the database:
```bash
flask db init
flask db migrate
flask db upgrade
```

## Running the Application

1. Start the Flask development server:
```bash
python main.py
```

2. Open your browser and navigate to:
```
http://localhost:5000
```

## Project Structure

```
resume-website/
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── script.js
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── blog.html
│   └── blog_post.html
├── main.py
├── models.py
└── README.md
```

## Features in Detail

### Theme Toggle
- Light and dark mode support
- Theme persistence using localStorage
- Smooth transition effects

### Blog System
- SQLite database integration
- Post creation and retrieval
- Responsive blog cards
- Individual post views

### Portfolio Section
- Project showcases with descriptions
- Technology stack badges
- Links to GitHub and live demos
- Hover animations

### Responsive Navigation
- Fixed-top navbar
- Mobile-friendly collapsible menu
- Active state tracking
- Smooth scroll behavior

## Development

### Adding Blog Posts

To add new blog posts, use the SQLite database:

```python
from main import app, db
from models import BlogPost

with app.app_context():
    new_post = BlogPost(
        title='Your Title',
        content='Your Content'
    )
    db.session.add(new_post)
    db.session.commit()
```

### Customization

1. **Styling**: Modify `static/css/style.css` for custom styles
2. **Content**: Update `templates/index.html` for personal information
3. **Theme**: Adjust CSS variables in `style.css` for theme colors

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For any queries or suggestions, please reach out through:
- GitHub: [SrkPrasadChangala](https://github.com/SrkPrasadChangala)
- LinkedIn: [Siva Rama Krishna Prasad Changala](https://www.linkedin.com/in/siva-rama-krishna-prasad-changala-a3115a253/)
- Email: minimalist1012@gmail.com
