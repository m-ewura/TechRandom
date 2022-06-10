##### Limit access to your deployed application on gcloud by setting up IAP Access

* Navigate to Security > Identity Aware Proxy > Enable API
> _Before you can use IAP, you need to configure your OAuth consent screen. The consent screen will be shown to users when requested to provide their private data._

* If OAuth consent screen is set, refresh browser and turn on IAP.
> _Status field should mark as correct after IAP is turned on._

* Select the checkbox corresponding to App Engine app. On the right side panel, and Add Principal.

* Add the email addresses of groups or individuals you want to grant IAP access to the project.
> _Role should be IAP-Secured Web App User role._

* Save.

**What happens now is that, only users listed here can access your project.**