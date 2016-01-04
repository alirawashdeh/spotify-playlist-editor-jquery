
# Spotify Playlist Editor

WunderVoice

## Configuration

Create an app at [Spotify Developer](https://developer.spotify.com/)

Modify the following part of the index.js file to include your client ID and client secret:

```
var client_id = 'CLIENT_ID_GOES_HERE'; // Your client id
var client_secret = 'CLIENT_SECRET_GOES_HERE'; // Your client secret
```

Once you have deployed your application, take a note of the URL and update the following part of the app.js file:

```
var redirect_uri = 'https://www.DEPLOYED_APP.com/callback';
```

Remember, OAuth requires that callback URLs are hosted using SSL, so ensure that you specify an "HTTPS" URL.

Make sure you then configure the same callback URL against your application at [Spotify Developer](https://developer.spotify.com/).

# Credits

Thanks to heroku/node-js-getting-started, spotify/web-api-auth-examples and the [OpenShift 'nodejs' cartridge](http://openshift.github.io/documentation/oo_cartridge_guide.html#nodejs)for the vast majority of this code.
