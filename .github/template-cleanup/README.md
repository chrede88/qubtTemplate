# %NAME%

Please follow the instructions below to finish the setup of your new Qubt site.

## Installation

0) Add a LICENSE to your repo.
1) Clone your version of the template to your local computer:
```shell
git clone https://github.com/%USER%/%NAME%
```
2) Change the module name to match your github repo in `go.mod`.
3) Modify `config/_default/hugo.yaml` and `config/_default/params.yaml` according to the Configuration below.
4) In a terminal/commandline, move to the newly created folder using `cd`.
5) Build a local version of your site by executing `hugo server`. You can see the site by navigating to `http://localhost:1313/%NAME%/` (actual URL will be outputted in the CLI) in a browser.
6) Add a new image to the `assets/` folder, using the same name as you specified in `params.yaml`.
7) Add a new `icon.png` file to update the favicon. The png file should be 512px by 512px in size.

---

## Configuration

All configuration is done in the four configuration files under `config/_default/`. The URL and site title can be set in `hugo.yaml`. The navbar settings are set in `menus.yaml`. All other parameters are set in `params.yaml`.

`hugo.yaml`:
```yaml
baseURL: 'https://%USER%.github.io/%NAME%'
title: 'Qubt Theme'
```

`menus.yaml`:
```yaml
main:
- name: Home
  url: /
  weight: 10
- name: Blog
  url: /blog/
  weight: 20
- name: About
  url: /about/
  weight: 30
```

`params.yaml`:
```yaml
############################
## Author
############################

author:
  name: %USER%
  image: author.jpeg
  greeting: "A personal blog theme for Hugo :evergreen_tree:"
  icon: ":wave:"

############################
## Links
############################

links:
  - github: https://github.com/%USER%/%NAME%
  - link: https://github.com/%USER%/%NAME%#readme
 

###############################
## OpenGraph & Twitter Cards
###############################

title: %NAME%
description: "Demo site build with Qubt & Hugo"
images:
  - thumbnail.jpeg
```

Links are defined by the name (i.e. "github" or "facebook"). The names must match one of the supported link icons, see list below.

### Supported Social Icons
| **Supported Icons** | **Supported Icons** | **Supported Icons** | **Supported Icons** |
| --- | --- | --- | --- |
| amazon | apple | bandcamp | bitbucket | 
| bluesky | check-mark | codepen | dev |
| discord | dribbble | email | etsy |
| facebook | flickr | foursquare | github |
| gitlab | google | instagram | keybase |
| kickstarter | link | linkedin | mastodon |
| medium | orcid | patreon | paypal | pinterest |
| reddit | signal | skype | slack |
| snapchat | soundcloud | spotify | stack-exchange |
| stack-overflow | strava | telegram | tiktok |
| tumblr | twitch | untappd | website |
| whatsapp | windows | x-twitter | youtube |


### Custom Social Icons
Users can provide their own icons by placing a `.svg` image in `./assets/icons/` in their own repo. Creating folders when necessary. The image should be as circular as possible for the best result. Don't use spaces in the filename! Find all current icons [here](https://github.com/chrede88/qubt/tree/main/assets/icons).

---

## Update the Theme Version

The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/Chrede88/qubt@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. You can find the releases [here](https://github.com/Chrede88/qubt/releases). Please check if any breaking changes are listed under the release you want to update to, before proceeding.

---

## Deploy on Github Pages
You can very easily deploy your site using Github Pages. Included in this template is a Github Action workflow that will build and deploy your site to Github Pages automatically:+1:

You can find the workflow here `.github/deploymentWorkflow/buildDeploy.yml`. To use this, move it to `.github/workflows/`.

The workflow is already set up and ready to go, but go through it and spend some time to understand what's going on. Otherwise, it'll always be this black box of magic that you can't fix when it breaks!

Last step: Go to Settings -> Pages -> Build and deployment -> Set the Source to "Github Actions".

Next time you publish a release this workflow will build and deploy your site :tada:

Your site will be published to the following URL:
`https://%USER%.github.io/%NAME%`