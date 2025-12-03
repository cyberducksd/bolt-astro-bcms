# Bun Marketing Website Example

A simple, component-driven marketing website built with **Astro** and **Bun** to help you learn the basics of modern web development.

## 🥟 About This Project

This project demonstrates how to build a component-driven marketing website using Bun as the JavaScript runtime. It showcases:

- **Component-based architecture** - Reusable UI components
- **Modern styling** - Scoped CSS with responsive design
- **Fast development** - Powered by Bun's blazing fast runtime
- **Static site generation** - Build for performance

## 🚀 Getting Started

### Prerequisites

Install Bun if you haven't already:

```bash
curl -fsSL https://bun.sh/install | bash
```

### Installation

```bash
# Install dependencies
bun install

# Start development server
bun run dev
```

Visit `http://localhost:4321` to see your site!

## 📁 Project Structure

```text
/
├── public/
│   └── favicon.svg          # Site favicon
├── src/
│   ├── assets/
│   │   ├── bun-logo.svg     # Bun logo asset
│   │   └── background.svg   # Background decoration
│   ├── components/
│   │   ├── Navbar.astro     # Navigation component
│   │   ├── Hero.astro       # Hero section component
│   │   ├── Features.astro   # Features grid container
│   │   ├── FeatureCard.astro # Individual feature card
│   │   ├── CodeExample.astro # Code snippet display
│   │   ├── CallToAction.astro # CTA section
│   │   └── Footer.astro     # Footer component
│   ├── layouts/
│   │   └── Layout.astro     # Base page layout
│   └── pages/
│       └── index.astro      # Main marketing page
└── package.json
```

## 🧩 Component Guide

### Understanding Component-Driven Development

Each component in this project is self-contained with its own:
- **Props** - Input data the component accepts
- **Template** - HTML structure
- **Styles** - Scoped CSS that won't leak to other components

### Example: Creating a New Component

```astro
---
// MyComponent.astro
interface Props {
  title: string;
  description?: string;
}

const { title, description = "Default description" } = Astro.props;
---

<div class="my-component">
  <h2>{title}</h2>
  <p>{description}</p>
  <slot /> <!-- Renders child content -->
</div>

<style>
  .my-component {
    padding: 1rem;
    background: white;
    border-radius: 8px;
  }
</style>
```

### Using Components

```astro
---
import MyComponent from '../components/MyComponent.astro';
---

<MyComponent title="Hello">
  <p>This content goes in the slot!</p>
</MyComponent>
```

## 🧞 Commands

All commands are run from the root of the project:

| Command          | Action                                       |
| :--------------- | :------------------------------------------- |
| `bun install`    | Install dependencies                         |
| `bun run dev`    | Start dev server at `localhost:4321`         |
| `bun run build`  | Build production site to `./dist/`           |
| `bun run preview`| Preview build locally before deploying       |

## 🎨 Customization Ideas

1. **Add new pages** - Create files in `src/pages/` (e.g., `about.astro`)
2. **Modify colors** - Update the gradient colors in component styles
3. **Add animations** - Use CSS transitions or add a library like Motion
4. **Create new components** - Build a testimonials section or pricing table
5. **Add content** - Connect to a CMS or use Astro's content collections

## 📚 Learn More

- [Bun Documentation](https://bun.sh/docs)
- [Astro Documentation](https://docs.astro.build)
- [Bun + Astro Guide](https://docs.astro.build/en/recipes/bun/)

## 🤝 Why Bun + Astro?

- **Bun** provides a fast JavaScript runtime, package manager, and bundler
- **Astro** delivers excellent static site performance with component islands
- Together they create a lightning-fast development and build experience

---

Built with ❤️ using Bun and Astro
