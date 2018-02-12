The gateway supports OTA documents containing "Browser settings" or
"Browser bookmarks", compatible with the Nokia/Ericsson
"Over The Air Settings Specification", with support up to v7.0.

This specification can be downloaded from the developer area of either
the Nokia or Ericsson web sites.

To create an OTA document, store the document in this directory with
a file extension of ".OTA".

To send an OTA "Browser settings" file to a mobile phone, use the
following URL format:

http://127.0.0.1:8800/?PhoneNumber=xxxxxxxx&OTA=filename

The "OTA" parameter specifies the name of a file located in the OTA
subdirectory of the gateway with a file extension of ".OTA".  For
example, in the above sample URL, the gateway would attempt to
locate a file named "filename.OTA" in the OTA gateway subdirectory.

To send an OTA "Browser bookmarks" file to a mobile phone, use the
following URL format:

http://127.0.0.1:8800/?PhoneNumber=xxxxxxxx&OTABookmark=filename

The "OTABookmark" parameter uses the same format as the "OTA"
parameter when sending "Browser settings", except that it expects
the browser bookmark settings file to have a file extension of “.BM”.

An example OTA "Browser settings" file is shown below, for additional
information, please refer to the Nokia/Ericsson "Over The Air Settings
Specification".


GSM/CSD Settings Example:

<?xml version="1.0" encoding="UTF-8"?>
<CHARACTERISTIC-LIST>
   <CHARACTERISTIC TYPE="ADDRESS">
      <PARM NAME="BEARER" VALUE="GSM/CSD"/>
      <PARM NAME="PROXY" VALUE="12.34.56.78"/>
      <PARM NAME="CSD_DIALSTRING" VALUE="+12135551212"/>
      <PARM NAME="PPP_AUTHTYPE" VALUE="PAP"/>
   </CHARACTERISTIC>
   <CHARACTERISTIC TYPE="URL" VALUE="http://mobileinternet.ericsson.com"/>
   <CHARACTERISTIC TYPE="NAME">
      <PARM NAME="NAME" VALUE="Mobile Internet"/>
   </CHARACTERISTIC>
   <CHARACTERISTIC TYPE="BOOKMARK">
      <PARM NAME="NAME" VALUE="Mobile Internet"/>
      <PARM NAME="URL" VALUE="http://mobileinternet.ericsson.com"/>
   </CHARACTERISTIC>
</CHARACTERISTIC-LIST>


