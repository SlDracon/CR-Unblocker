# CR-Unblocker

## What is the CR-Unblocker?
The CR-Unblocker is a browser extension for removing the region lock on Crunchyroll. It was originally developed by Onestay for Chrome and I've ported it to Edge. You can find the original repo [here](https://github.com/Onestay/CR-Unblocker).

## How does it work?
The CR-Unblocker will get an American Session ID and set it as your current Session ID cookie. Like this Crunchyroll will think you are located in the US and therefore you have access to all the anime you couldn't watch.

## I've heard it isn't safe?
The method all Crunchyroll Unblockers are using is basically the same as described above. Your session id is bound to your account after being set as a cookie. However, I take security very serious. The server the backend server is running on is secure. If you notice anything suspicious *PLEASE* tell me.

Please note: I'm not responsible for any compromised accounts.

## Installing
Just download the extension from your browsers store:
- [Microsoft Edge](https://www.microsoft.com/store/apps/9PF520KDMZRZ)
- [Google Chrome](https://chrome.google.com/webstore/detail/cr-unblocker/agapeeilkibacbfeijlidlgppmjaaijn)

The Chrome extension is not uploaded or maintained by me, that's done by [Onestay](https://github.com/Onestay).

## Setting the server up yourself
If you are really concerned about security you can run the server getting Session IDs yourself. I will give you a brief tutorial here but can't help you with every little detail:

1. You should have some knowledge of NodeJS
2. Clone the repo
3. Assuming you got NPM and NodeJS setup, move package.json, getSessionId.js and server.js to your VPS or something like that hosted in America. I can recommend running the server behind a reverse proxy like Nginx.
4. run `npm install`, `node server.js` and setup Nginx
5. In extension/background_script.js set the URL of the fetch to the URL of your own server
6. Add the extension folder as an unpacked extension to your browser.

## Contributing
The extension is currently still under development. If you have any idea on what to add feel free to contribute to this project or the [original project](https://github/Onestay/CR-Unblocker).
