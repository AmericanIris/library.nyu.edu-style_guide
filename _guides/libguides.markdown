---
breadcrumbs: true
title: LibGuides Widgets Embeds
layout: article
published: true
---

## Copy & Paste libguides embed code

Copy the "embed code" from the Libguides widgets interface into your Siteleaf markdown page. It will look something like the following:

<textarea rows="15" style="font-family:monospace">
<script type="text/javascript" src="//lgapi-us.libapps.com/web/jquery/js/1.12.1_jquery.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/jquery/js/1.9.2_jquery-ui.min.js"></script>
<script type="text/javascript" src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.4/js/bootstrap.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/js1.15.5/springshare.public.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/js1.15.5/springshare.common.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/js1.15.5/common/springspace_sui_helptip.js"></script>
<link rel="stylesheet" href="//lgapi-us.libapps.com/web/jquery/css/1.8.24_themes_base_jquery-ui.css" />
<link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css" />
<link rel="stylesheet" href="//lgapi-us.libapps.com/web/css1.15.5/springshare.public.min.css" />
<link rel="stylesheet" href="//lgapi-us.libapps.com/web/css1.15.5/springshare.common.min.css" />
<link href="//maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
<link href="//lgapi-us.libapps.com/web/css1.15.5/common/springspace_sui_helptip.css" rel="stylesheet"><script src="//lgapi-us.libapps.com/sa.php?site_id=873" onload="springSpace.springTrack.init({_st_site_id: '873'});"></script>
<script>springSpace.Common = springSpace.Common || { };
springSpace.Common.constant = { PROCESSING: { ACTION_DISPLAY_POLL: 159	}};
springSpace.Common.baseURL = "//lgapi-us.libapps.com/";
springSpace.Common.apiLoad = true;</script><script>
springshare_widget_config_1486571185568 = { path: 'boxes/8930090' };
</script>
<div id="s-lg-widget-1486571185568"></div>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://lgapi-us.libapps.com/widgets.php?site_id=873&widget_type=8&output_format=1&widget_title=Open+Positions+at+NYU+Libraries&widget_height=250&widget_width=100%25&widget_embed_type=1&guide_id=425839&box_id=8930090&map_id=10526582&content_only=0&config_id=1486571185568";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","s-lg-widget-script-1486571185568");</script>
</textarea>

## Manually delete Libguides scripts and styles

There are a lot of excess `<script>` and `<link>` tags here. The former embed Libguides specific Javascript and the latter embed Libguides specific stylesheets. We'll want to remove both of these in order to use the native scripts and stylesheets on the website.

Delete everything from the beginning of the first `<script>` tag to the end of the last `<link>` tag. This means keep the `<script>` tag that looks like `<script src="//lgapi-us.libapps.com/sa.php?site_id=...>`. Note the `src` pointing to `sa.php`. That one is essential to the embed working.

This means you will delete the following lines:

<textarea rows="15" style="font-family:monospace">
<script type="text/javascript" src="//lgapi-us.libapps.com/web/jquery/js/1.12.1_jquery.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/jquery/js/1.9.2_jquery-ui.min.js"></script>
<script type="text/javascript" src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.4/js/bootstrap.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/js1.15.5/springshare.public.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/js1.15.5/springshare.common.min.js"></script>
<script type="text/javascript" src="//lgapi-us.libapps.com/web/js1.15.5/common/springspace_sui_helptip.js"></script>
<link rel="stylesheet" href="//lgapi-us.libapps.com/web/jquery/css/1.8.24_themes_base_jquery-ui.css" />
<link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css" />
<link rel="stylesheet" href="//lgapi-us.libapps.com/web/css1.15.5/springshare.public.min.css" />
<link rel="stylesheet" href="//lgapi-us.libapps.com/web/css1.15.5/springshare.common.min.css" />
<link href="//maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
<link href="//lgapi-us.libapps.com/web/css1.15.5/common/springspace_sui_helptip.css" rel="stylesheet">
</textarea>

## Resulting embed code

The final script should look something like the following:

<textarea rows="15" style="font-family:monospace">
<script src="//lgapi-us.libapps.com/sa.php?site_id=873" onload="springSpace.springTrack.init({_st_site_id: '873'});"></script>
<script>springSpace.Common = springSpace.Common || { };
springSpace.Common.constant = { PROCESSING: { ACTION_DISPLAY_POLL: 159	}};
springSpace.Common.baseURL = "//lgapi-us.libapps.com/";
springSpace.Common.apiLoad = true;</script><script>
springshare_widget_config_1486571185568 = { path: 'boxes/8930090' };
</script>
<div id="s-lg-widget-1486571185568"></div>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://lgapi-us.libapps.com/widgets.php?site_id=873&widget_type=8&output_format=1&widget_title=Open+Positions+at+NYU+Libraries&widget_height=250&widget_width=100%25&widget_embed_type=1&guide_id=425839&box_id=8930090&map_id=10526582&content_only=0&config_id=1486571185568";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","s-lg-widget-script-1486571185568");</script>
</textarea>
