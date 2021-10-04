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



## 2. Replace macros on third party tags

* Replace the cache busting macro with our own macro **[RANDOM]**
* Replace the GDPR macro with 0
 
 ## 3. Escaping third party tags
 
 * Escape javascript tag with the help of json escaping tool 

    Here is a screenshot of **escaped** third party tag

![App Screenshot](https://user-images.githubusercontent.com/81978167/134903843-06bc1a88-0f14-47bd-831a-276c89134855.png)

## 4. Creating campaign.json file

* Create campaign.json file under the main folder of the campaign and move the folder to  ad.populus-media.net/2021 in local git repository
* Write proper height, width, ctype of the image and paste the escaped tag under adTgas within " "


sample campaign.json file is shown below

~~~

{
   "active": true,
   "reportingKey": "UA-157372883-11",
   "weights": "1",
   "subs": {
      "300x250": {
         "type": "3",
         "width": "300px",
         "height": "250px",
         "adTags": [
            "<ins class='dcmads' style='display:inline-block;width:300px;height:250px'\r\n    data-dcm-placement='N266802.3768237POPULUSMEDIAINC.\/B26423391.314189835'\r\n    data-dcm-rendering-mode='iframe'\r\n    data-dcm-https-only\r\n    data-dcm-gdpr-applies='gdpr=0'\r\n    data-dcm-gdpr-consent='gdpr_consent=${GDPR_CONSENT_755}'\r\n    data-dcm-addtl-consent='addtl_consent=${ADDTL_CONSENT}'\r\n    data-dcm-ltd='false'\r\n    data-dcm-resettable-device-id=''\r\n    data-dcm-app-id=''>\r\n  <script src='https:\/\/fw.adsafeprotected.com\/rjss\/www.googletagservices.com\/821927\/57322740\/dcm\/dcmads.js'><\/script>\r\n<\/ins>\r\n"
         ]
      }
   }   
}

~~~



## Site served creatives

Site-served creatives are raw HTML or image files that are hosted by publishers instead of advertisers. We may receive one or more zipped HTML files or image files representing the creatives

## Steps for setting up HTML tag

1. The HTML tag can be in zip folder or the client can send the folder normally
2. Unzip the folder and move the file to the github local repository in the path ad.populus-media.net/2021 
3. Test the HTML tag by running a local server and in the HTML tag tester tool
4. Make sure to fix the dimensions like height, width and border of the tag as required 
5. Use `<iframe src="put tag url here"></iframe>` and test the tag in the HTML tag tester tool
6. If the tag is working properly, the tag must be escaped with the help of json escaping tool
   
   sample of escaped HTML tag
   ~~~
    <iframe src=\"https:\/\/ad.populus-media.net\/2021\/compass\/2021_Compass_Patient_728x90_HTML5_Banner\/\" style=\"border:none\", width=\"728\", height=\"90\"><\/iframe>
    ~~~

7. Create a campaign.json file inside the main folder 
8. In campaign.json file enter the height, width, ctype, and put the escaped tag under adTags within " "
9. Save the file poperly after the completing the campaign.json  
    
    sample campaign.json file 
    
 ~~~
    
{
   "active": true,
   "reportingKey": "UA-157372883-11",
   "weights": "1",
   "subs": {
      "728x90": {
         "type": "3",
         "width": "728px",
         "height": "90px",
         "adTags": [
            "<iframe src=\"https:\/\/ad.populus-media.net\/2021\/compass\/2021_Compass_Patient_728x90_HTML5_Banner\/\" style=\"border:none\", width=\"728\", height=\"90\"><\/iframe>"
         ]
      }
   }   
}
    
~~~~



## steps for setting up image tag

1. The image tag can be in zip folder or the client can send the folder normally
2. Unzip the folder and move the file to the github local repository in the path ad.populus-media.net/2021
3. The images can be either in jpeg format or png format. 
4. Test the images by gunning a local server or in the HTML tag tester tool
5. Make sure to fix the dimensions like height, width of the image and remove the border if there
6. For generating the HTML tag of the image, copy the url from the browser
7. Use `<img src="paste url of the image"></img>` and preview this tag in the HTML tag tester tool
   
   sample of esacped image tag
    ~~~
    <img src=\"https:\/\/ad.populus-media.net\/2021\/helloworld\/image_300x250.jpeg\" style=\"border:none\", height=\"250\", width=\"300\"><\/img>
    ~~~
    
8. If the tag is working properly, the tag must be escaped with the help of json escaping tool
9. Create a campaign.json file inside the main folder 
10. In campaign.json file enter the height, width, ctype and the put the escaped tag under ad.tags within " "
11. save the file properly after compleating the campaign.json
 



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
