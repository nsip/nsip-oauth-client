***DEPRECATED (RETIRED)***

*This repository is obsolete and retired (archived). This is an unmantained repository. In particular, note that it is not being updated with security patches, including those for dependent libraries.*




Example oauth2orize Consumer
===

This is an oauth2 consumer that uses `passport-oauth` and `passport-oauth2`
to communicate with any oauth2 provider.
In particular, this is meant to be paired with the
[example oauth2orize provider](https://github.com/jaredhanson/oauth2orize/tree/master/examples/all-grants).

Installation
===

    npm install -g jade

    git clone https://github.com/coolaj86/example-oauth2orize-consumer.git
    pushd example-oauth2orize-consumer/
    npm install
    jade public/*.jade

Usage
===

Edit `./example-oauth2orize-consumer.js` to point to your desired oauth2 provider and then run the server.

    node ./server 3001

Then visit <http://localhost:3001> and play around.

NSIP modifications
===

Local and provider configuration has been completely moved to the configuration
files {local,provider}-config.js (respectively). Sample configurations are
provided in the .dist files.

local-config.js contains the protocol and host on which the OAuth 2 client
(i.e. the web server, relying party, etc) is running.

provider-config.js contains information for the OAuth 2 server: its address,
and the client ID and secret. Note that the OAuth endpoints are hard-coded to
/oauth/authorize and /oauth/token; these match the accompanying
nsip-oauth-server package.

