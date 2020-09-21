# Tablacus Explorer Icon Packs
Icon packs for Tablacus Explorer

## Structure

### Folders and files
```
┣ config.json
┣ preview.png (Optional)
┃
┣ general (Optional)
┃　┣ 0.png
┃　┣ 1.png
┃　┣    ：
┃
┣ browser (Optional)
┃　┣ 0.png
┃　┣ 2.png
┃　┣    ：
┃
┣ shell32 (Optional)
┃　┣ 0.png
┃　┣ 11.png
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
- **URL:** is optional.
- **icons:** is optional.
- **size:** is the size of the icon in pixels (Optional)
- **max:** is the number of the last icon (Optional)

### General icons
![image](https://user-images.githubusercontent.com/5156977/93665978-8bd15d80-fab5-11ea-87be-23ffe9295c2b.png)

`bitmap:ieframe.dll,216,16,4` → `general\4.png`

`bitmap:ieframe.dll,214,24,4` → `general\4.png`

### Browser icons
![image](https://user-images.githubusercontent.com/5156977/93665999-ab688600-fab5-11ea-967e-9111c5a638e9.png)

`bitmap:ieframe.dll,206,16,18` → `browser\18.png`

`bitmap:ieframe.dll,204,24,18` → `browser\18.png`

### shell32 icons
![image](https://user-images.githubusercontent.com/5156977/93666031-d6eb7080-fab5-11ea-9a74-2449e5047f10.png)

`icon:shell32.dll,12` → `shell32\12.png`

You only need to prepare the icons you want to replace.

The default icon will be used for the missing parts.

The icon size should be around 48px to 96px, but you can set it to any number in config.json.

The `preview.png` will appear on the download list page to help the user choose an icon set.

## User Interface

Downloading icon packs can be done from inside the Tablacus UI like addons

 ![image](https://user-images.githubusercontent.com/5156977/93667643-8595ae00-fac2-11ea-8e6f-2738fec8604e.png)
 
 It will have a separate download page in gallery format with previews
　|　
-|-
![image](https://user-images.githubusercontent.com/5156977/93691921-130ae980-fb27-11ea-8091-3b0054cd92e7.png)|**Icon Pack A Name**<br>Creator<br>Description<br>…………<br>…………<br>![image](https://user-images.githubusercontent.com/5156977/93692109-f7551280-fb29-11ea-808c-87fc3b7b94fe.png)<br>
![image](https://user-images.githubusercontent.com/5156977/93691921-130ae980-fb27-11ea-8091-3b0054cd92e7.png)|**Icon Pack B Name**<br>Creator<br>Description<br>…………<br>…………<br>![image](https://user-images.githubusercontent.com/5156977/93692109-f7551280-fb29-11ea-808c-87fc3b7b94fe.png)<br>
![image](https://user-images.githubusercontent.com/5156977/93691921-130ae980-fb27-11ea-8091-3b0054cd92e7.png)|**Icon Pack C Name**<br>Creator<br>Description<br>…………<br>…………<br>![image](https://user-images.githubusercontent.com/5156977/93692109-f7551280-fb29-11ea-808c-87fc3b7b94fe.png)<br>
