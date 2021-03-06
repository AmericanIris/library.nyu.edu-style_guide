---
breadcrumbs: true
title: Color
layout: article
published: true
---

<div class="style-guide__colors">
  <h1>Text</h1>

  <p class="text_black">
    <input class="color-val" type="text" />
    Black - <code>$text_black</code><br />
    <strong>Used for:</strong> Base style for all text
  </p>

  <p class="text_dark_gray">
    <input class="color-val" type="text" />
    Dark gray - <code>$text_dark_gray</code><br />
    <strong>Used for:</strong> Tabs and "See more" links
  </p>

  <p class="text_light_gray">
    <input class="color-val" type="text" />
    Light gray - <code>$text_light_gray</code><br />
    <strong>Used for:</strong> Meta text
  </p>

  <p class="text_footer_white">
    <input class="color-val" type="text" />
    Footer White - <code>$text_footer_white</code><br />
    <strong>Used for:</strong> Base footer text
  </p>

  <p class="text_footer_dark_gray">
    <input class="color-val" type="text" />
    Footer Gray - <code>$text_footer_dark_gray</code><br />
    <strong>Used for:</strong> Deemphasized footer text
  </p>

  <p class="text_blue">
    <input class="color-val" type="text" />
    Blue - <code>$text_blue</code><br />
    <strong>Used for:</strong> Links
  </p>

  <p class="text_light_blue">
    <input class="color-val" type="text" />
    Light blue - <code>$text_light_blue</code><br />
    <strong>Used for:</strong> Hovered links
  </p>

  <p class="text_green">
    <input class="color-val" type="text" />
    Green - <code>$text_green</code><br />
    <strong>Used for:</strong> Icons
  </p>

  <p class="text_lavendar">
    <input class="color-val" type="text" />
    Lavendar - <code>$text_lavendar</code><br />
    <strong>Used for:</strong> Deemphasized header text
  </p>

  <hr /><h1>Borders</h1>

  <p class="border_dotted_gray">
    <input class="color-val" type="text" />
    Dotted border gray - <code>$border_dotted_gray</code><br />
    <strong>Used for:</strong> Dotted borders
  </p>

  <p class="border_solid_gray">
    <input class="color-val" type="text" />
    Solid border gray - <code>$border_solid_gray</code><br />
    <strong>Used for:</strong> Solid borders
  </p>

  <p class="border_footer">
    <input class="color-val" type="text" />
    Footer border - <code>$border_footer</code><br />
    <strong>Used for:</strong> Footer borders
  </p>

  <hr /><h1>Backgrounds</h1>

  <p class="background_black">
    <input class="color-val" type="text" />
    Black background - <code>$background_black</code><br />
    <strong>Used for:</strong> Footer background
  </p>

  <p class="background_light_gray">
    <input class="color-val" type="text" />
    Light gray background - <code>$background_light_gray</code><br />
    <strong>Used for:</strong> Banner and zebra striped table background
  </p>

  <p class="background_field_gray">
    <input class="color-val" type="text" />
    Light gray field background - <code>$background_field_gray</code><br />
    <strong>Used for:</strong> Form field background
  </p>

  <hr /><h1>Misc.</h1>

  <p class="purple">
    <input class="color-val" type="text" />
    Purple - <code>$purple</code><br />
    <strong>Used for:</strong> Header and button background and generic message icons
  </p>

  <p class="purple_dark">
    <input class="color-val" type="text" />
    Dark Purple - <code>$purple_dark</code><br />
    <strong>Used for:</strong> Pressed button background
  </p>

  <p class="purple_light">
    <input class="color-val" type="text" />
    Light Purple - <code>$purple_light</code><br />
    <strong>Used for:</strong> Hovered button background
  </p>

  <p class="red">
    <input class="color-val" type="text" />
    Red - <code>$red</code><br />
    <strong>Used for:</strong> Alert message icons
  </p>
</div>

<script type="text/javascript">
  var hexDigits = new Array
          ("0","1","2","3","4","5","6","7","8","9","a","b","c","d","e","f");

  //Function to convert hex format to a rgb color
  function rgb2hex(rgb) {
   rgb = rgb.match(/^rgb\((\d+),\s*(\d+),\s*(\d+)\)$/);
   return "#" + hex(rgb[1]) + hex(rgb[2]) + hex(rgb[3]);
  }

  function hex(x) {
    return isNaN(x) ? "00" : hexDigits[(x - x % 16) / 16] + hexDigits[x % 16];
   }

  var fields = document.querySelectorAll('.color-val');
  for (var i = fields.length - 1; i >= 0; i--) {
    var field = fields[i];
    var style = window.getComputedStyle(field);
    var rgb = style.backgroundColor;
    field.value = rgb2hex(rgb);
  }
</script>
