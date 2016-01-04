
# Spotify Playlist Editor

The Spotify Playlist Editor is a node.js web application that allows Spotify users to rearrange tracks in their playlists online.

Currently hosted at (www.playlisteditor.com)[www.playlisteditor.com]

### But why?
Currently, the Android Spotify app doesn't allow you reorder tracks in your playlists - this must be carried out on the desktop application or iOS app.

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

## Deploying to Open Shift

Ensure that you have the [OpenShift Client Tools](https://developers.openshift.com/en/managing-client-tools.html) installed and configured.

Run the following commands, remembering to give a unique application name in place of <app_name>

$ cd spotify-playlist-editor
$ rhc app create <app_name> nodejs-0.10

You then need to [configure SSL](https://developers.openshift.com/en/managing-domains-ssl.html) before the Spotify OAuth callback will work.

## Credits

Thanks to heroku/node-js-getting-started, spotify/web-api-auth-examples and the [OpenShift 'nodejs' cartridge](http://openshift.github.io/documentation/oo_cartridge_guide.html#nodejs)for the vast majority of this code.
