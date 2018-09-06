# SharePointAppOnlyApp
This Project contains an sharepoint app that access sharepoint online using AppId and Secret. Creating AppOnly Permissions Conole App.
You can copy the code from the console app and use it in your App.

This project is a sample on how to access SharePoint without service accounts through Apps. Since it is not recommended to access SharePoint using user accounts, we have to access SP in a different way. We can register the App in SharePoint which generates a Secret and that provides access to SharePoint.

Below are the steps to create AppId and Secret in SharePoint:

1. Use the following link to generate AppId. In the URL, please replace &lt;sitecollection&gt; with your sitecollection https://&lt;sitecollection&gt;/_layouts/15/AppRegNew.aspx
2. 
  
 In the Permissions Request XMl, paste the below XML:
  
  &lt;AppPermissionRequests AllowAppOnlyPolicy="true"&gt;<br>
   &lt;AppPermissionRequest Scope="http://sharepoint/content/sitecollection" Right="FullControl" /&gt;<br>
 &lt;/AppPermissionRequests&gt;
