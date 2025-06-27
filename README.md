# Personal Portfolio Website

A responsive, modern personal portfolio website built with HTML, CSS, JavaScript, and Tailwind CSS.

## Features

- Responsive design for all device sizes
- Dark/light mode toggle
- Four main pages: Home, About, Portfolio, Contact
- Project filtering on Portfolio page
- Form validation on Contact page
- Smooth scrolling and animations
- SEO optimized with meta tags
- Accessible design following WCAG guidelines

## Technologies Used

- HTML5
- CSS3 (with Tailwind CSS)
- JavaScript
- Tailwind CSS (via CDN)
- Google Fonts (Poppins)
- Formspree for contact form submissions

## Getting Started

### Prerequisites

- Web browser (Chrome, Firefox, Safari, Edge)
- Code editor (VS Code recommended)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/portfolio-website.git
   ```

2. Open the project folder in your code editor.

3. Open `index.html` in your browser to view the website locally.

## Deployment

This website can be deployed to any static hosting service:

### Netlify

1. Drag and drop the project folder to Netlify's drop zone.
2. Follow the prompts to complete deployment.

### Vercel

1. Install Vercel CLI:

   ```bash
   npm install -g vercel
   ```

2. Deploy:

   ```bash
   vercel
   ```

## Customization

To personalize this portfolio:

1. Replace placeholder content in HTML files with your own information.
2. Update images in the `assets/images` folder.
3. Change colors in Tailwind classes to match your brand.
4. Update the Formspree form action URL in `contact.html` with your own Formspree endpoint.

## File Structure

```
portfolio-website/
├── index.html          # Homepage
├── about.html          # About page
├── portfolio.html      # Portfolio page
├── contact.html        # Contact page
├── assets/
│   ├── css/
│   │   └── style.css   # Custom CSS (if needed)
│   ├── js/
│   │   └── main.js     # Main JavaScript file
│   └── images/         # All images
├── README.md           # Project documentation
└── robots.txt          # SEO file
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Tailwind CSS for utility-first styling
- Unsplash for placeholder images
- Formspree for form handling
- Google Fonts for typography
