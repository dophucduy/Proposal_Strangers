# Hugo Site with Learn Theme

## Setup Instructions

1. **Install Hugo**: Download from https://gohugo.io/installation/
2. **Install Theme**: 
   ```bash
   cd themes
   git clone https://github.com/matcornic/hugo-theme-learn.git
   ```
3. **Run Development Server**:
   ```bash
   hugo server -D
   ```

## Project Structure

- `content/` - Your markdown content files
- `static/` - Static assets (images, CSS, JS)
- `layouts/` - Custom layout templates
- `themes/` - Hugo themes
- `hugo.toml` - Site configuration

## Adding Content

Create new pages by adding `.md` files to the `content/` directory. Use front matter to set title, weight, and other properties.

## Theme Features

The Learn theme provides documentation-focused features like search, navigation, and notice boxes.