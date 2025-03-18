---
layout: default
title: Configuration
nav_order: 2
---

# Configuration
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Site Configuration

The site configuration is managed through the `_config.yml` file. Here are the key settings you can customize:

### Basic Settings

```yaml
title: Your Site Title
description: Your site description
theme: just-the-docs
```

### URL Configuration

```yaml
url: https://username.github.io/repository
```

### Navigation

```yaml
# Aux links for the upper right navigation
aux_links:
  "View on GitHub":
    - "https://github.com/username/repository"

# Enable or disable the site search
search_enabled: true

# Heading anchor links
heading_anchors: true
```

### Theme Settings

```yaml
# Color scheme
color_scheme: light # or dark

# Enable or disable copy button on code blocks
enable_copy_code_button: true
```

## Local Development

To run the site locally:

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Start the local server:
   ```bash
   bundle exec jekyll serve
   ```

3. Visit `http://localhost:4000` in your browser

## Customization

### Custom CSS

Create a file at `_sass/custom/custom.scss` to add your own styles:

```scss
// Add your custom styles here
.custom-class {
  color: #123456;
}
```

### Custom JavaScript

Add custom JavaScript by creating `_includes/head_custom.html`:

```html
<script type="text/javascript">
  // Your custom JavaScript here
</script>
``` 