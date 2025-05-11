# Astro Daisy Theme Toggle
Component to add a dark and light theme to your AstroJS and DaisyUI project.

## Features
- Use any [DaisyUI theme](https://daisyui.com/docs/themes/#list-of-themes)
- If an invalid theme is used it will default to DaisyUIs dark and light theme
- Use with or without AstroJS View Transitions
- No Flash of Unstyled Content
- Use with any [DaisyUI theme controller](https://daisyui.com/components/theme-controller/)

## Installation

1. Install Tailwind CSS
2. Install DaisyUI
3. ```npm install astro-daisy-theme-toggle```

## Usage
1. Import the DaisyTheme component. It takes two props. darkTheme sets the dark theme and lightTheme sets the light theme. The component must wrap around any DaisyUI theme controller. Theme controllers have a value prop that can be removed or left in place. It will be ignored.

```astro
---
import { DaisyTheme } from 'astro-daisy-theme-toggle'
---
<DaisyTheme darkTheme='forest' lightTheme='fantasy'>
    <input type='checkbox' value='synthwave' class='toggle theme-controller' />
</DaisyTheme>
```

2. Add the same themes you used in the DaisyTheme component to your DaisyUI plugin.

```css
@plugin "daisyui" {
  themes:
    fantasy --default,
    forest --prefersdark;
}
```
