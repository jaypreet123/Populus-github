# Third party tags

A third-party ad tag is simply a snippet of Javascript code, generated from a 3rd party ad server, which is then placed into an ad inventory space on a website or app to display ad creatives that were uploaded on the ad server.

## Setting up third party tags

* For setting third party tags, javascript tag is verified and previewed whether the add is running in the third party server or not.



  
## Sample tag:

```<script type="text/adtag">
<ins class='dcmads' style='display:inline-block;width:728px;height:90px'
    data-dcm-placement='N848755.3768237POPULUSMEDIAINC./B24929807.295286034'
    data-dcm-rendering-mode='script'
    data-dcm-https-only
    data-dcm-gdpr-applies='gdpr=${GDPR}'
    data-dcm-gdpr-consent='gdpr_consent=${GDPR_CONSENT_755}'
    data-dcm-addtl-consent='addtl_consent=${ADDTL_CONSENT}'
    data-dcm-resettable-device-id=''
    data-dcm-app-id=''>
  <script src='https://www.googletagservices.com/dcm/dcmads.js'></scr+ipt>
</ins>
</script>
<script language="javascript" type="text/javascript" src="https://cdn.doubleverify.com/dvbs_src.js?ctx=17280832&cmp=24929807&plc=295286034&sid=6114862&dvregion=0&unit=728x90">
</script>
```

  * After preview the javascript tag is escaped with a json escape tool.
  
## HTML tags:


## Screenshot of escaping tag:

![App Screenshot](https://user-images.githubusercontent.com/81978167/134119283-8bd60dfd-9ef3-47bb-b39a-0766aa464bfb.png)

 ## How to implement third party tag in campaign.json file:

  * The escaped code is copied to the campaign.json file under adTags. 
  * campaign.json file contains objects, properties, keys, width, height and weight.
  * There can be one or more properties under single object.
  * Finally the code in the saved and pushed in the github repository (ad.populus-media.net).

  
## Screenshot of campaign.json file:

![App Screenshot](https://user-images.githubusercontent.com/81978167/134121816-67976274-bc9e-4852-908d-65e86c8f324c.png)
