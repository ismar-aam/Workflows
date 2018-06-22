Add Feature Workflow/Delete Feature Workflow
Geocortex Essentials version 3.9+
Silverlight Viewerer version 1.5.2+

BACKGROUND:
These workflows were developed by David Flack at Ruekert-Mielke with lots of help from Victoria McDonald at Latitude Geographics.  These workflows automate the process of placing and deleting features and do not require the Editing Toolbar.  The primary motivation for these tools is to simplify the UX for non-technical staff who have editing needs.

USAGE:
These workflows are typical in terms of their use in a site.  See https://support.geocortex.com/publishing-workflows-in-the-silverlight-viewer for more information regarding how to publish workflows and make them accessible in the Silverlight Viewer.
 
For both features, it is assumed a feature layer is already present in the site.  It also has token security.  Simply delete the Generate Token tasks if this is not necessary in your environment.

-AddPoint.xaml.  This workflow is used for adding features.  Simply configure the following variables in the workflow:
	un: username (if you need to generate tokens)
	pwd: password (if you need to generate tokens)
	tokenServiceURL: token service URL (if you need to generate tokens)
	featureLayerURL: REST URL of your feature layer
	mapServiceID: ID of your site.xml feature layer- used for refreshing the map after adding.
	
This workflow demonstrates adding point geometry.  If a different geometry is needed, that can be specified in the Capture 	Geometry task.

-DeletePoint.xaml.  This workflow is used for deleting points.  You'll need to configure the following variables
	un: username (if you need to generate tokens)
	pwd: password (if you need to generate tokens)
	tokenServiceURL: token service URL (if you need to generate tokens)
	featureLayerURL: REST URL of your feature layer
	mapServiceID: ID of your site.xml feature layer- used for refreshing the map after deletion.

This workflow demonstrates deletion by selecting a rectangle geometry.  If a different geometry is needed, that can be 	specified in the Capture Geometry task. Also, this workflow contains a few commented alerts that demonstrate a few good places to check for problems in this process.

FURTHER DEVELOPMENT:
No further development is planned at this time.  A logical extension to the AddPoint workflow is to pop up the attribute editing form, but was not necessary in this use case.  Also, a modify feature workflow may be beneficial as well.

We hope these workflows provide some assistance to the Geortex user community.