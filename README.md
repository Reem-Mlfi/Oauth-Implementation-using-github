# Oauth-Implementation-using-github
## in this app outh is implemented using github.com 

## following the steps:

### Users are redirected to request their GitHub identity
#### When your GitHub App specifies a login parameter, it prompts users with a specific account they can use for signing in and authorizing your app.
#### client_id :The client ID you received from GitHub when you registered.
#### redirect_uri: The URL in your application where users will be sent after authorization. See details below about redirect urls.
#### login:Suggests a specific account to use for signing in and authorizing the app.
#### scope: A space-delimited list of scopes. If not provided, scope defaults to an empty list for users that have not authorized any scopes for the application. For users who have authorized scopes for the application, the user won't be shown the OAuth authorization page with the list of scopes. Instead, this step of the flow will automatically complete with the set of scopes the user has authorized for the application. For example, if a user has already performed the web flow twice and has authorized one token with user scope and another token with repo scope, a third web flow that does not provide a scope will receive a token with user and repo scope.
#### state: An unguessable random string. It is used to protect against cross-site request forgery attacks.
#### allow_signup: Whether or not unauthenticated users will be offered an option to sign up for GitHub during the OAuth flow. The default is true. Use false when a policy prohibits signups.

### Users are redirected back to your site by GitHub
#### If the user accepts your request, GitHub redirects back to your site with a temporary code in a code parameter as well as the state you provided in the previous step in a state parameter. The temporary code will expire after 10 minutes. If the states don't match, then a third party created the request, and you should abort the process.
#### client_id: The client ID you received from GitHub for your OAuth App.
#### client_secret: The client secret you received from GitHub for your OAuth App.
#### code: The code you received as a response to Step 1.
#### redirect_uri: The URL in your application where users are sent after authorization.
#### Get Accept access token as a response.

### Your app accesses the API with the user's access token
#### The access token allows you to make requests to the API on a behalf of a user.
