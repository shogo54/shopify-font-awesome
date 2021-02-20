# Shopify Font Awesome

If your Shopify theme is missing Font Awesome or has older version of it, use this to integrate Font Awesome to your store in no time!

## How to setup

Follow the steps below to setup Font Awesome on your Shopify theme.

### Preparation 

Make sure that you remove the Font Awesome from your theme if there's one already integrated. If you have trouble doing this, check FAQ. 

### Asset uploads

Download this repository, and upload all the files from the assets folder into your theme assets.

### Integration

Open your theme's Layout > theme.liquid, and add the following code into your header.

```liquid
  <!-- Font-Awesome ================================================== -->
  {{ 'all.min.css' | asset_url | stylesheet_tag }}
```

### That's it!

Now you can use Font Awesome anywhere on your store. Take a look at these [examples](http://fortawesome.github.io/Font-Awesome/examples/). And [all the awesome icons to choose from](http://fortawesome.github.io/Font-Awesome/icons/)!

### For more info

Check out the official site: [http://fontawesome.io](http://fontawesome.io)

## FAQ

### What if I want to use different version of Awesome Font?

- Find a version of Font Awesome that you want to use in [here](https://github.com/FortAwesome/Font-Awesome/releases)
- Download the zip folder, extract them, and find "webfonts" folder. 
- Upload everything in that folder to your theme's assets folder.
- Go to "css" folder in your downloaded Font Awesome folder, and look for ```fontawesome.min.css``` or ```all.min.css```. Upload the file to your theme's assets folder as well. 
- Go to your theme's layout > theme.liquid. In your header, add the following lines. Replace YOUR_AWESOME_FONT_FILE_NAME to the file name matching the file you found. 
```liquid
  <!-- Font-Awesome ================================================== -->
  {{ 'YOUR_AWESOME_FONT_FILE_NAME' | asset_url | stylesheet_tag }}
```
- That's all!

### My theme has an older version of Font Awesome but I want to upgrade it to a newer version. 

- You need to remove the Font Awesome from your theme first. 
- Take a look at layout > theme.liquid, and search for ```.css``` or ```font-awesome```. If you find any, remember the name of the file and remove the lines that include it. 
- Then go to assets folder. Find any files that has file name starting with ```fa```, ```FontAwesome```, or ```fontawesome```. Get rid of them with the css file that you found in the theme.liqud.
- Now you are good to go. Go ahead and integrate whatever version of Font Awesome to your theme!



