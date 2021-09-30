## Third Party Tags

A third-party ad tag is simply a snippet of Javascript code, generated from a 3rd party ad server, which is then placed into an ad inventory space on a website or app to display ad creatives that were uploaded on the ad server.

Here is an example of a third party tag

~~~~~
<script type="text/adtag">
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
~~~~~
### Steps

#### 1. Preview third party tag to make sure rendering correctly



#### 2. Replace macros on third party tags

* Replace the cache busting macro with our own macro **[RANDOM]**
* Replace the GDPR macro with 0
 
 #### 3. Escaping third party tags
 
 * Escape javascript tag with the help of json escaping tool 

    Here is a screenshot of **escaped** third party tag

![App Screenshot](https://user-images.githubusercontent.com/81978167/134903843-06bc1a88-0f14-47bd-831a-276c89134855.png)

## Site served creatives

Site-served creatives are raw HTML or image files that are hosted by publishers instead of advertisers. We may receive one or more zipped HTML files or image files representing the creatives

steps for setting up HTML tag

1. The HTML tag can be in zip folder or the client can send the folder normally
2. Unzip the folder and move the file to the github local repository in the path ad.populus-media.net/2021 
3. Test the HTML tag by running a local server or in the HTML tag tester tool
4. Make sure to fix the dimensions like height, width and border of the tag as required 
5. Use <iframe src="put tag url here"></iframe> and test the tag in the HTML tag tester tool
6. If the tag is working properly, the tag must be escaped with the help of json escaping tool
7. 
8. Create a campaign.json file inside the main folder 
9. 

* Site served tag is concatenated with third party tag and escaped
* The escaping process remains the same for all tags

### HTML tag

HTML tags are like keywords which defines that how web browser will format and display the content. With the help of tags, a web browser can distinguish between an HTML content and a simple content. HTML tags contain three main parts: opening tag, content and closing tag.

Steps for setting up HTML tag




 ## How to implement third party tag in campaign.json file:

  * The escaped code is copied to the campaign.json file under adTags. 
  * campaign.json file contains objects, properties, keys, width, height and weight.
  * There can be one or more properties under single object.
  * Finally the code in the saved and pushed in the github repository (ad.populus-media.net).

  
## Screenshot of campaign.json file:

![App Screenshot](https://user-images.githubusercontent.com/81978167/134121816-67976274-bc9e-4852-908d-65e86c8f324c.png)
