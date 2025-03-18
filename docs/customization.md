---
layout: default
title: Customization
nav_order: 5
has_children: false
permalink: /docs/customization
---

# Customization
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Theme Configuration

### Color Scheme

You can customize the color scheme by modifying your `_config.yml` file:

```yaml
# Color scheme supports "light" (default) and "dark"
color_scheme: dark

# Customize the light mode color scheme
light_theme_color: "#007bff"  # Primary color for light mode
```

### Site Logo

Add your custom logo by updating the `_config.yml`:

```yaml
# Logo file (default is title text)
logo: "/assets/images/logo.png"

# Set a path/url to a favicon that will be displayed by the browser
favicon_ico: "/assets/images/favicon.ico"
```

## Custom CSS

### Adding Custom Styles

Create a new file `_sass/custom/custom.scss` to add your custom styles:

```scss
// Custom styles
$link-color: #007bff;
$btn-primary-color: #0056b3;

// Override default styles
.site-title {
  font-weight: 700;
  color: $link-color;
}

.navigation-list-item {
  &.active {
    background-color: lighten($link-color, 45%);
  }
}
```

### Custom Layout

You can create custom layouts in the `_layouts` directory:

```html
<!-- _layouts/custom.html -->
---
layout: default
---
<div class="custom-layout">
  {% raw %}{{ content }}{% endraw %}
  <div class="custom-sidebar">
    <!-- Your sidebar content here -->
    <nav class="custom-nav">
      <ul>
        <li><a href="#section1">Section 1</a></li>
        <li><a href="#section2">Section 2</a></li>
      </ul>
    </nav>
  </div>
</div>
```

## Navigation Customization

### Custom Navigation Structure

Modify the navigation structure in your `_config.yml`:

```yaml
# Enable or disable the site search
search_enabled: true

# Aux links for the upper right navigation
aux_links:
  "Just the Docs on GitHub":
    - "//github.com/just-the-docs/just-the-docs"

# Makes Aux links open in a new tab
aux_links_new_tab: true
```

### Custom Navigation Order

Control the order of navigation items using the `nav_order` front matter:

```yaml
---
layout: default
title: My Page
nav_order: 2
---
```

## Footer Customization

### Custom Footer Content

Create a custom footer by adding `_includes/footer_custom.html`:

```html
<footer class="site-footer">
  <div class="footer-content">
    <p>&copy; 2024 Your Company. All rights reserved.</p>
    <div class="footer-links">
      <a href="/privacy">Privacy Policy</a>
      <a href="/terms">Terms of Service</a>
    </div>
  </div>
</footer>
```

## Advanced Customization

### Custom JavaScript

Add custom JavaScript by creating `assets/js/custom.js`:

```javascript
// Custom JavaScript
document.addEventListener('DOMContentLoaded', function() {
  // Your custom JavaScript code
});
```

Include it in your layout:

```html
<script src="{% raw %}{{ '/assets/js/custom.js' | relative_url }}{% endraw %}"></script>
```

### Custom Components

Create reusable components in `_includes` directory:

```html
<!-- _includes/alert.html -->
<div class="alert alert-{% raw %}{{ include.type }}{% endraw %}">
  {% raw %}{{ include.message }}{% endraw %}
</div>
```

Use the component in your pages:

```markdown
{% raw %}{% include alert.html type="warning" message="This is a warning message" %}{% endraw %}
```

### Custom Plugins

Add custom Jekyll plugins in the `_plugins` directory:

```ruby
# _plugins/custom_tag.rb
module Jekyll
  class CustomTag < Liquid::Tag
    def render(context)
      "This is a custom tag"
    end
  end
end

Liquid::Template.register_tag('custom_tag', Jekyll::CustomTag)
```

## Search Customization

### Custom Search Configuration

Modify search settings in `_config.yml`:

```yaml
# Enable or disable the search feature
search_enabled: true

# Maximum amount of previews per search result
search_previews: 3

# Maximum amount of words to display before a matched word in the preview
search_tokenizer_separator: /[\s/]+/
```

### Exclude Pages from Search

Add front matter to exclude specific pages:

```yaml
---
layout: default
title: Hidden Page
search_exclude: true
---
```

## Image Usage

### Basic Image

You can add images to your documentation using standard Markdown syntax or with additional styling classes:

```markdown
![Example image](/assets/images/example-image.png)
```

### Image with Styling

Add custom classes to control image appearance:

```markdown
![Example image with styling](/assets/images/example-image.png){: .img-example .border .shadow }
```

### Responsive Images

Make images responsive to container width:

```markdown
![Responsive example](/assets/images/example-image.png){: .img-fluid }
```

### Image Alignment

Control image alignment using utility classes:

```markdown
![Left aligned image](/assets/images/example-image.png){: .float-left .mr-2 }
![Center aligned image](/assets/images/example-image.png){: .d-block .mx-auto }
![Right aligned image](/assets/images/example-image.png){: .float-right .ml-2 }
``` 