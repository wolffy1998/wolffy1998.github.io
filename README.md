# Wolffy1998 - Personal Homepage

Personal portfolio website hosted on GitHub Pages at [wolffy1998.github.io](https://wolffy1998.github.io).

## Structure

```
.
├── index.html          # Main homepage
├── css/
│   └── style.css       # Stylesheets
├── js/
│   └── main.js         # JavaScript for interactivity
├── .github/
│   └── workflows/
│       └── deploy.yml  # CI/CD for GitHub Pages
├── .nojekyll           # Disable Jekyll processing
└── README.md
```

## Features

- Responsive design (mobile, tablet, desktop)
- Dark theme with modern UI
- Project showcase cards with tags and links
- Contact section with social links
- Smooth scrolling navigation
- CSS animations and transitions

## Customization

Edit the following to personalize:

1. **index.html** - Update project cards, social links, email, and bio text
2. **Avatar** - Replace the hero-avatar image URL with your GitHub avatar
3. **Projects** - Modify project names, descriptions, tags, and links
4. **Contact** - Update email address and social media URLs

## Deployment

This site uses GitHub Actions for automated deployment:

1. Push to the `main` branch
2. GitHub Actions will automatically build and deploy
3. Go to your repository **Settings > Pages** and select:
   - Source: **GitHub Actions**
4. Visit `https://wolffy1998.github.io`

## License

MIT
