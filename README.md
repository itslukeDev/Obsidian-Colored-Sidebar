# Obsidian-Colored-Sidebar v2.0.0

## A Colored Sidebar CSS Snippet for Obsidian

### _Create a [colorfully cascading](https://youtu.be/rAkerV8rlow) Obsidian sidebar!_

![Example](./example.png)

This snippet targets folders beginning with numbered prefixes and applies full color formatting based on the root colors listed inside the snippet. The prefixes are both customizable and extensible; feel free to change, add, and remove them based on your own titles and vault structure!

By default, the snippet includes 8+1 colors, with additional common colors provided as a starting point for your own customization. Simply swap out the color variable names in the prefix variables to customize your sidebar's appearance.

## Installation

1. Open Obsidian and navigate to `Settings -> Appearance`
2. Scroll down to the "CSS Snippets" section
3. Click the "Open Snippets Folder" button
4. Place the `Colored Sidebar Items.css` file from this repository into the opened folder
5. Back in Obsidian, click the "Reload Snippets" button
6. Toggle on the "Colored Sidebar Items" snippet

See the [How It Works](#how-it-works) section below to complete the setup in your vault.

## How It Works

The snippet targets folders beginning with numbered prefixes (00 through 07, plus 99). These prefixes have assigned color values inside the CSS file and form a continuous gradient when lined up together (with the exception of 99).

> [!IMPORTANT]
> Make sure to prepend your folder names with these prefixes for the colors to work!

### Customizing Colors

1. Open the CSS snippet in your preferred text editor
2. Locate the `root` section
3. Find the color variables with their hexadecimal code values
4. To modify a color, replace the hex value with your new color value
5. To add a new color, follow the existing pattern and add a new variable in this section

### Customizing Prefixes

1. Looking under the `.theme-light` and `.theme-dark` properties you can the prefix variables. There you can specify what color should be used for what prefix for both themes
2. Further down in the CSS file, you’ll see the CSS class names targeting folders, named something like `.nav-folder-title[data-path^="00"]`.
   - Each colored group has four classes targeting the same prefix.
   - To change prefixes:
     - Replace the numbers in quotations with any other number, letter, or word.
     - For advanced selector modifications, see [this CSS selectors guide](https://css-tricks.com/almanac/selectors/a/attribute/)

### Adding Additional Folders

1. Copy one of the groups of CSS classes that target the same prefix
2. Change the duplicated prefix and replace any instance of a prefix variable (e.g., `--prefix-01`) with your desired color variable

> [!NOTE]
> Several built-in color variables are included but not used by default. These are from a matching palette that you're welcome to use for expanding your colored sidebar!

---

> [!TIP]  
> This snippet pairs excellently with the [Iconize](https://github.com/FlorianWoelki/obsidian-iconize) plugin!

_Inspired by the "Coloured Folders" snippet by Lithou._
