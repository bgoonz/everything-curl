# everything-curl


* [WEBSITE](https://bgoonz.github.io/everything-curl/)




# Introduction #

An introduction to [`curl`](http://curl.haxx.se/) using [GitHub's API](https://developer.github.com/guides/getting-started/#overview).

# The Basics #

Makes a basic GET request to the specifed URI

    curl https://api.github.com/users/bgoonz

Includes HTTP-Header information in the output

    curl --include https://api.github.com/users/bgoonz

Pass user credential to basic auth to access protected resources like a users starred gists, or private info associated with their profile

    curl --user "bgoonz:PASSWD" https://api.github.com/gists/starred
    curl --user "bgoonz:PASSWD" https://api.github.com/users/bgoonz

Passing just the username without the colon (`:`) will cause you to be prompted for your account password. This avoids having your password in your command line history

    curl --user "bgoonz" https://api.github.com/users/bgoonz

## POST ##

Use the `--request` (`-X`) flag along with `--data` (`-d`) to POST data

    curl --user "bgoonz" --request POST --data '{"description":"Created via API","public":"true","files":{"file1.txt":{"content":"Demo"}}' https://api.github.com/gists
    
    curl --user "bgoonz" -X POST --data '{"description":"Created via API","public":"true","files":{"file1.txt":{"content":"Demo"}}' https://api.github.com/gists

Of course `--data` implies POST so you don't have to also specify the `--request` flag

    curl --user "bgoonz" --data '{"description":"Created via API","public":"true","files":{"file1.txt":{"content":"Demo"}}' https://api.github.com/gists

Here is an example that uses the old GitHub API (v2). You can use multiple `--data` flags

    curl --data "login=bgoonz" --data "token=TOKEN" https://github.com/api/v2/json/user/show/bgoonz

The post data gets combined into one so you can also just combine them yourself into a single `--data` flag

    curl --data "login=bgoonz&token=TOKEN" https://github.com/api/v2/json/user/show/bgoonz

You can tell curl to read from a file (`@`) to POST data

    curl --user "bgoonz" --data @data.txt https://api.github.com/gists 

Or it can read from STDIN (`@-`)

    curl --user "bgoonz" --data @- https://api.github.com/gists
    {
      "description":"Test",
      "public":false,
      "files": {
        "file1.txt": {
          "content":"Demo"
        }
      }
    }
    end with ctrl+d

### Headers ###

Often when POSTing data you'll need to add headers for things like auth tokens or setting the content type. You can set a header using `-H`.

    curl -H "Content-Type: application/json" -H "authToken: 349ab29a-xtab-423b-a5hc-5623bc39b8c8" --data '{}' https://api.example.com/endpoint


### Dealing with HTTPS ###

If an API doens't have an SSL cert but is using HTTPS you can tell curl to ignore the security by using `--insecure`. Be warned this is a very **"insecure"** thing to do and is only listed here for "educational purposes".

    curl --insecure https://api.example.com/endpoint

For my own reference mostly, here is where I first learned about using `--insecure` https://github.com/wayneeseguin/rvm/issues/1684

# OAuth #

The first thing to know is that your API Token (found in https://github.com/settings/admin) is not the same token used by OAuth. They are different tokens and you will need to generate an OAuth token to be authorized.

Follow the API's instructions at http://developer.github.com/v3/oauth/ under the sections "Non-Web Application Flow" and "Create a new authorization" to become authorized.

Note: Use Basic Auth once to create an OAuth2 token http://developer.github.com/v3/oauth/#oauth-authorizations-api

    curl https://api.github.com/authorizations \
    --user "bgoonz" \
    --data '{"scopes":["gist"],"note":"Demo"}'

This will prompt you for your GitHub password and return your OAuth token in the response. It will also create a new Authorized application in your account settings https://github.com/settings/applications

Now that you have the OAuth token there are two ways to use the token to make requests that require authentication (replace "OAUTH-TOKEN" with your actual token)

    curl https://api.github.com/gists/starred?access_token=OAUTH-TOKEN
    curl -H "Authorization: token OAUTH-TOKEN" https://api.github.com/gists/starred

List the authorizations you already have

    curl --user "bgoonz" https://api.github.com/authorizations


# Resources #

* HTTParty - Ruby library that makes it easy to create HTTP requests https://github.com/jnunemaker/httparty
* Hurl IT - An open source web application to play with curl options http://hurl.it
