# Entscheidung zur Heilung - Podcast Website

A Hugo-based podcast website using the [Castanet](https://github.com/mattstratton/castanet) theme.

## Prerequisites

- [Hugo](https://gohugo.io/getting-started/installing/) (extended version recommended)
- Git

## Getting Started

1. Clone this repository with submodules:
   ```bash
   git clone --recurse-submodules https://github.com/your-username/entscheidung-zur-heilung-podcast-website.git
   ```

2. If you already cloned without submodules, initialize them:
   ```bash
   git submodule update --init --recursive
   ```

3. Start the development server:
   ```bash
   hugo server -D
   ```

4. Open your browser at `http://localhost:1313`

## Building for Production

```bash
hugo
```

The generated site will be in the `public/` directory.

## Project Structure

```
├── archetypes/          # Content templates
├── content/             # Site content
│   ├── about/          # About page
│   ├── episode/        # Podcast episodes
│   ├── guest/          # Guest profiles
│   └── host/           # Host profiles
├── data/               # Data files
├── layouts/            # Custom layouts
├── static/             # Static assets (images, audio, etc.)
├── themes/
│   └── castanet/       # Castanet theme (git submodule)
└── hugo.toml           # Site configuration
```

## Adding New Episodes

Create a new markdown file in `content/episode/`:

```markdown
+++
Description = "Episode description"
author = "host"
date = "2024-01-15T10:00:00+01:00"
episode = "1"
episode_image = "img/episode/default.jpg"
explicit = "no"
podcast_duration = "30:00"
podcast_file = "your-episode-file.mp3"
title = "Episode Title"
+++

Episode content goes here...
```

## Configuration

Edit `hugo.toml` to customize:
- Site title and description
- Navigation menu
- Social media links
- Podcast feed settings
- Theme appearance

## License

See the [Castanet theme license](https://github.com/mattstratton/castanet/blob/master/LICENSE) for theme-specific licensing.