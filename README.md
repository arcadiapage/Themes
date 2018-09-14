# Themes

This repo documents the specs of the theme format used across the Hundred Rabbits' [ecosystem](https://github.com/hundredrabbits). You can also implement the theme support into your own apps. See the [Collection](COLLECTION.md) for all available themes.

<img src='https://raw.githubusercontent.com/hundredrabbits/Themes/master/PREVIEW.jpg' width='600'/>

## Setup

Install Themes support, by adding [theme.js](https://github.com/hundredrabbits/Dotgrid/blob/master/desktop/sources/scripts/lib/theme.js) to your header. Define the overrides in a [dedicated theme.css](https://github.com/hundredrabbits/Dotgrid/blob/master/desktop/sources/links/theme.css) by adding this line to your header.

```
<script type="text/javascript" src="scripts/lib/theme.js"></script>
<link rel="stylesheet" type="text/css" href="links/theme.css"/>
```

Initiate the Theme class by adding these lines somewhere in your project.

```
let theme = new Theme();
theme.install(document.body);
theme.start();
```

**Theme.js** will add a handler that will detect files dragged onto the project, and append a `<style>` element to your document's body element with the theme overrides.

## Specs

- `background`, Background, general.
- `f_high`, Foreground, high-contrast.
- `f_med`, Foreground, medium-contrast.
- `f_low`, Foreground, low-contrast.
- `f_inv`, Foreground, inverted.
- `b_high`, Background, high-contrast.
- `b_med`, Background, medium-contrast.
- `b_low`, Background, low-contrast.
- `f_inv`, Background, inverted.

## The Theme Format

The theme file format is an SVG file. The [theme.js](https://github.com/hundredrabbits/Dotgrid/blob/master/desktop/sources/scripts/lib/theme.js) loader will look for colors found in the element's `id` attributes.

```
<svg width="96px" height="64px" xmlns="http://www.w3.org/2000/svg" baseProfile="full" version="1.1">
  <rect width='96' height='64'  id='background' fill='#E0B1CB'></rect>
  <!-- Foreground -->
  <circle cx='24' cy='24' r='8' id='f_high' fill='#231942'></circle>
  <circle cx='40' cy='24' r='8' id='f_med' fill='#5E548E'></circle>
  <circle cx='56' cy='24' r='8' id='f_low' fill='#BE95C4'></circle>
  <circle cx='72' cy='24' r='8' id='f_inv' fill='#E0B1CB'></circle>
  <!-- Background -->
  <circle cx='24' cy='40' r='8' id='b_high' fill='#FFFFFF'></circle>
  <circle cx='40' cy='40' r='8' id='b_med' fill='#5E548E'></circle>
  <circle cx='56' cy='40' r='8' id='b_low' fill='#BE95C4'></circle>
  <circle cx='72' cy='40' r='8' id='b_inv' fill='#9F86C0'></circle>
</svg>
```

## Supported Applications

- [Marabu](https://github.com/hundredrabbits/Marabu), music tool.
- [Left](https://github.com/hundredrabbits/Left), writing tool.
- [Dotgrid](https://github.com/hundredrabbits/Dotgrid), vector tool.
- [Donsol](https://github.com/hundredrabbits/Donsol), card game.

This collection may also be used with
[Tape](https://aeriform.itch.io/tape) by Aeriform.

## Extras

You are welcome to submit your own themes to this collection!

