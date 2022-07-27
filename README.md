# participatory-mapping
testing participatory mapping with Google Forms and Leaflet

## testing demo
https://jackdougherty.github.io/participatory-mapping/

**ISSUE: this demo code seems to have hard-coded responses rather than collecting user data**

Google Form public view
https://docs.google.com/forms/d/e/1FAIpQLSfgy2P7FZNbFn1_DdTN6j7UuTyT_F_RgKS4u0-wFeS2fstj3g/viewform

Google Form author view
https://docs.google.com/forms/d/1p2zm6g9cCGzJVE2DpbAnHQFceM5127HyIjRd3s4FlKo/edit

Linked Google Sheet responses
https://docs.google.com/spreadsheets/d/1D6skRCvkF4DNIAlbpGhbLxCF5rSAH4U9GV_32Twxibs/edit#gid=155169481

Published Google Sheet of responses
https://docs.google.com/spreadsheets/d/e/2PACX-1vT-BkdLXpNn6-VA4wzs5bvUvEfFl8P-sUfN5-5Lf8NV4blrEYbWQN-Sci8Ov52XHepy6x6QBNwyW4NG/pubhtml

## Credits
Adapted from https://github.com/HarryatBigWater/harryatbigwater/tree/master/participatory_mapping_planning (unlicensed), who adapted it from https://aogdp.github.io/gpsform/ (unlicensed), with these [OLD instructions from aogdp](https://github.com/aogdp/gpsform/blob/gh-pages/README.md)

## Instructions-in-progress
1. Fork a copy of the code from GitHub
2. Open the original Google Form, and make a copy to your Google Drive. The original contains short-answer questions for: ip address, markerA, markerB, markerC. *Unclear if IP address is appropriate to collect, and format of other variables*
3. In your new Google Form > Responses, create a new linked Google Sheet in your Google Drive to collect responses
3. Make a copy of the Google Sheet (with responses to your Google Form) to your Google Drive
4. [Pre-fill](https://support.google.com/docs/answer/160000?hl=en) your Google Form to create appropriate variables for your responses. *Unclear about format of variables*
5. [File>Share>Publish](https://support.google.com/docs/answer/37579?hl=en) your Google Sheet responses to the web


*Old instructions:* The prefilled form will look something like this:
```
https://docs.google.com/forms/d/formId/viewform?entry.field1=39.01&entry.field2=-81.26&entry.field3=description
```
In the code repo, open `map_survey.html` and change these variables to match yours:
*Old instructions:*
*ISSUES*
*Unclear if formID comes from Published or Author view*
```javascript
 var formId = 'Your Form Id';
 var formLat = 'Longitude id from prefilled form';
 var formLng = 'Latitude id from prefilled form';
 var formText = 'Description id from prefilled form';
 var gsheet = 'sheet id';
```
*Also see Google formResponse ID hardcoded around line 364*

Host your updated code on the web using GitHub Pages or your own webserver.

##Enhancements
Could be added but I wanted to keep this app as simple as possible.

1. Add styling using Awesome Markers, Maki Markers or other plugins.
2. Add search.
3. More basemaps.
5. Layer selector.
6. Figure out a way to collect pictures taken with the device, and push that url to the google sheet. This would take much more coding than is in the initial app. I suggest this be accomplished manually.
