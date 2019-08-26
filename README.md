# Missive GCal Export Integration

Adds an integration to the [Missive mail app](https://missiveapp.com/) that parses emails for dates/times
and displays them to export to Google Calendar if desired. Clicking the export button will
automatically open Google Calendar's "New Event" page and allow you to customize fields' content. Three files (`index.html`, `main.js`,
`theme.css`) need to be deployed to a server that the Missive app can reach. A sample is deployed
on [my website](https://zachhardesty.com/missive) or you can run the integration from source on a local server by executing `yarn
start` after changing the text following the `tunnel` command [on line 21 of `package.json`](package.json#L21) from `--subdomain
missive-gcal` to `--subdomain [YOUR TEXT]`. The local server sometimes fails to start due to a bug
with `localtunnel`, just run `yarn start` again.

## Activating the Integration

- open the Missive desktop app
- click on your profile at the bottom left
- click `Integrations` in the flyover menu
- click `Add integration` at the bottom of the modal
- select the `Custom` option with a gear at the bottom of the list
- enter `Name` & `iFrame URL` as...
  - Name: `Google Calendar Export`
  - iFrame URL: `https://[YOUR TEXT].localtunnel.me` or `https://zachhardesty.com/missive` or url of
    your server that's hosting the previously mentioned 3 files
- Close modal

## Preview

light

![sidebar-light](https://i.imgur.com/KTrw9or.png)

dark

![sidebar-dark](https://i.imgur.com/aETnd8F.png)

## Acknowledgements

[chrono](https://github.com/wanasit/chrono) - natural language processing with a focus on dates and
times

[ESLint](https://github.com/eslint/eslint) - enforce my favorite styles

[ftp-deploy](https://github.com/simonh1000/ftp-deploy) - helpful for deploying integration to your
server and simpler than other tools

[live-server](https://github.com/tapio/live-server) - ultra simple quick local server with
hot-reloading for testing

[localtunnel](https://github.com/localtunnel/localtunnel) - allow Missive to access your local
server

[npm-run-all](https://github.com/mysticatea/npm-run-all) - run the server and the tunnel in parallel
in 1 terminal

*Copyright (c) 2019 || Zach Hardesty || [zachhardesty.com](https://zachhardesty.com)*
