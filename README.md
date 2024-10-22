# DDMCS - Idee progetto <br>

*Influenza di post di influencer che promuovono prodotti fake per dimagrimento e quando gli adolescenti (soprattutto femmine) vanno poi a comprare questi prodotti e sono interessati a provare queste cose (ultimo si può fare tramite analisi dei commenti sotto i post/video). <br>
Social network da analizzare: Instagram, TikTok(?)* <br>

Graph API per prendere dati:<br>
1. **`Set Up an Instagram Developer Account`** <br>
To access the Instagram Graph API, you'll first need to set up an Instagram Developer account:<br>
*`Create a Facebook Developer Account`*: Visit Facebook for Developers and log in with your Facebook account.<br>
*`Create an App`*: In your Facebook Developer dashboard, create a new app. Select "For Everything Else" as the app type. This app will be used to access the Instagram Graph API.<br>
*`Set Up Instagram Basic Display`*: In the app settings, configure "Instagram Basic Display" to allow access to public profile information, media, and other content.<br>

2. **`Get Access to Instagram Data via the API`** <br>
You can access data like public media, comments, and hashtags using the Instagram Graph API. Here’s a high-level overview:<br>
*`a) Request an Access Token`* <br>
You’ll need to generate an access token to authenticate your requests to the Instagram Graph API. This token is linked to your app and your Instagram Business or Creator account.<br>
*To generate an access token*:<br>
Go to the Tools & Support section of the Facebook Developer dashboard.<br>
Under Access Tokens, generate a short-lived token for development.<br>
Convert it into a long-lived token by making an API call, so that you don’t have to refresh it frequently.<br>
*`b) Link Instagram Account to Your App`* <br>
You need an Instagram Business or Creator account to access more detailed metrics. `To link it`:<br>
In Instagram settings, switch your account to either Business or Creator.<br>
Link your Instagram account to the Facebook Page that you’ll manage via the API.<br>
