---
title: Using RadEditor in Web Content Management scenario
page_title: Using RadEditor in Web Content Management scenario | UI for ASP.NET AJAX Documentation
description: Using RadEditor in Web Content Management scenario
slug: moss/sharepoint-2007-(moss)/radeditor-for-moss/installation-and-deployment/using-radeditor-in-web-content-management-scenario
tags: using,radeditor,in,web,content,management,scenario
published: True
position: 4
---

# Using RadEditor in Web Content Management scenario



Telerik RadEditor for MOSS can be easily used as a cross-browser rich-text editor for Web Content Management in SharePoint 2007. In order to replace the default editor in a page template, you need to perform a one-time modification using SharePoint Designer 2007. All content which has been authored through the default editor will be preserved and accessible through the Telerik RadEditor for MOSS.



## Using the new feature

>note  __NOTE:__ Once the RadEditor for MOSS features are activated they will affect only the current site. You need to activate the RadEditor features for each site individually. If you want to change the scope of the features, see the following article -[Change the RadEditor features scope]({%slug moss/sharepoint-2007-(moss)/radeditor-for-moss/configuration/change-the-radeditor-features-scope%})
>


1. From the __Site Actions__ menu go to __Site Settings > Modify All Site Settings__
>caption 

![](images/4_Lists1_thumb.png)

1. Click Site features in the Site Administration column
>caption 

![](images/SiteFeaturesMoss_thumb.png)

1. Scroll to the bottom of the list and activate the __Use RadEditor to edit HMTL fields__ feature.
>caption 

![](images/SiteFeaturesMoss2_thumb.png)

1. __IMPORTANT!__ If you still see the default editor or a simple textbox after you activate the RadEditor feature(s), you might need to open a command prompt window and type __iisreset__ to reset the Internet Information Server. This will prevent problems caused by caching.

## UsingSharePoint Designer

1. Open a page in the __Microsoft Office SharePoint Designer 2007__. Select the page you wish to modify and choose __Edit Page Layout__.
>caption 

![](images/5_WCM1_thumb.png)

1. At the top, after the default SharePoint Register tags add the following registration line (replace Version=x.x.x.x with the RadEditor for MOSS version, e.g for editor v5.12 use Version=5.1.2.0):<%@ Register TagPrefix="telerik" Namespace="Telerik.SharePoint.FieldEditor" Assembly="RadEditorSharePoint, Version=x.x.x.x, culture=neutral, PublicKeyToken=1f131a624888eeed" %>
>caption 

![
         
      ](images/5_WCM2_thumb.png)

1. Replace the tag of the default editor __<PublishingWebControls:RichHtmlField ... >__with the RadEditor tag:< telerik:RadHtmlField id="Content" FieldName="..." runat="server"></telerik:RadHtmlField>
>caption 

![](images/5_WCM3_thumb.png)

# See Also

 * [Using the RadEditor WebPart]({%slug moss/sharepoint-2007-(moss)/radeditor-for-moss/installation-and-deployment/using-the-radeditor-webpart%})

 * [Using RadEditor in List Items]({%slug moss/sharepoint-2007-(moss)/radeditor-for-moss/installation-and-deployment/using-radeditor-in-list-items%})