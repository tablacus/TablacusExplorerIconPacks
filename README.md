# Tablacus Explorer Icon Packs
Icon packs for Tablacus Explorer

## New
Added support for SVG files from Tablacus Explorer 22.2.9.

## Structure

### Folders and files
```
┣ config.json
┣ preview.png (Optional)
┃
┣ general (Optional)
┃　┣ 0.png (0.svg)
┃　┣ 1.png (1.svg)
┃　┣    ：
┃
┣ browser (Optional)
┃　┣ 0.png (0.svg)
┃　┣ 2.png (2.svg)
┃　┣    ：
┃
┣ shell32 (Optional)
┃　┣ 0.png (0.svg)
┃　┣ 11.png (11.svg)
┃　┣    ：
┃
…………………
```
### config.json
```
{
  "info": {
    "name": {
      "en": "Flat icons"
    },
    "descprition": {
      "en": "Flat icons set"
    },
    "creator": {
      "en": "Gaku"
    },
    "id": "Flat_icons",
    "ext": ".png",
    "version": "1.00",
    "pubDate" : "Thu, 17 Sep 2020 00:00:00 GMT",
    "license": "MIT License",
    "URL": "http://tablacus.github.io/TablacusExplorerAddons/"
  },
  "icons": {
    "general": {
      "size": 48,
      "max": 20
    },
    "browser": {
      "size": 48,
      "max": 10
    },
    "shell32": {
      "size": 48,
      "max": 30
    }
  }
}
```
- **ext** is the extension of the icon file (Default: .png)
- **URL:** is optional.
- **icons:** is optional.
- **size:** is the size of the icon in pixels (Optional)
- **max:** is the number of the last icon (Optional)

### General icons
![image](https://user-images.githubusercontent.com/5156977/93665978-8bd15d80-fab5-11ea-87be-23ffe9295c2b.png)

`icon:general,4` → `general\4.png` / `general\4.svg`

`bitmap:ieframe.dll,216,16,4` → `general\4.png` / `general\4.svg`

`bitmap:ieframe.dll,214,24,4` → `general\4.png` / `general\4.svg`

### Browser icons
![image](https://user-images.githubusercontent.com/5156977/93665999-ab688600-fab5-11ea-967e-9111c5a638e9.png)


`icon:browser,18` → `browser\18.png` / `browser\18.svg`

`bitmap:ieframe.dll,206,16,18` → `browser\18.png` / `browser\18.svg`

`bitmap:ieframe.dll,204,24,18` → `browser\18.png` / `browser\18.svg`

### shell32 icons
![image](https://user-images.githubusercontent.com/5156977/93666031-d6eb7080-fab5-11ea-9a74-2449e5047f10.png)

`icon:shell32.dll,12` → `shell32\12.png` / `shell32\12.svg`

You only need to prepare the icons you want to replace.

The default icon will be used for the missing parts.

The PNG icon size should be around 48px to 96px, but you can set it to any number in config.json.

The `preview.png` will appear on the download list page to help the user choose an icon set.

## User Interface

Downloading icon packs can be done from inside the Tablacus UI like addons

 ![image](https://user-images.githubusercontent.com/5156977/93667643-8595ae00-fac2-11ea-8e6f-2738fec8604e.png)
 
 It will have a separate download page in gallery format with previews

![image](https://user-images.githubusercontent.com/8735426/154456128-0d5c9e7e-1826-4e14-9857-b0f68caa5c80.png)

## Vector Icons

Tablacus supports [SVG](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics) based vector icons.
Vector graphics scale well to larger sizes. Because they are defined as shapes composed of points, lines, curves, fills and strokes, they never pixelate when enlarged.
Since vector icons are based on discrete elements rather than images, they are not static and may be styled to match the current theme as required.

While defining SVG icons for Tablacus you can use both styles and XML attributes to style your SVG elements. Any explicitly defined fill or stroke color will be respected. Themable elements that should change color according to Tablacus to match the current theme should use the variable `currentColor`.

In this example the first circle fill color is defined as red and is respected by Tablacus regardless of current theme; on the second circle the stroke is defined as `currentColor` so it will dynamically use Tablacus text color to correctly match light or dark themes and always be visible regardless of background.

```
<svg class="text" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="20" fill="#ff0000"/>
  <circle cx="50" cy="50" r="45" stroke="currentColor"/>
</svg>
```
|Light themes|Dark themes|
|---|---|
|![image](https://user-images.githubusercontent.com/5156977/153303536-1145737a-0fcd-4a85-b320-8e083205d365.png)|![image](https://user-images.githubusercontent.com/5156977/153303675-c08c5a91-a9bf-4c1b-876f-dee3e58aa1dd.png)|

Defining appearance as styles is also supported and taken into account for theming as well

```
<svg class="text" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="45" style="fill:#ff0000; fill-opacity:1"/>
  <circle cx="50" cy="50" r="20" style="stroke:currentColor; stroke-opacity:1"/>
</svg>
```

