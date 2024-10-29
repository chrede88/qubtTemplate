# Qubt - Template

This is the theme template repository! **Please** follow the installation instructions below.
If you're looking for the actual theme repository, follow this [link](https://github.com/Chrede88/qubt).

## Installation

1) Use this template by pressing `Use this template`. **Don't fork this repository!**
2) Wait 20s-30s and update the page. The files in your repo are getting populated.
3) Add a LICENSE to your repo.
4) Clone your version of the template to your local computer:
```shell
git clone https://github.com/<username>/<reponame>
```
5) Change the module name to match your github repo in `go.mod`.
6) Modify `config/_default/hugo.yaml`, `config/_default/params.yaml` and `config/_default/menus.yaml` according to the configuration below.
7) Add your blog posts to `content/blog/`. See example posts for reference.
8) Modify `content/about.md` so it matches your preferences.
9) All images are stored in the `assets/` folder. You can group in subfolders if you like.
10) Build a local version of your site by executing `hugo server`. You can see the site by navigating to `localhost:1313` (actual URL will be outputted in the CLI) in a browser.
11) Add a new `icon.png` file to update the favicon. The png file should be 512px by 512px in size.

---

## Features

- Simple personal blog theme, designed for mobile-first.
- Automatic dark mode (based on system setttings).
- Emoji support for a fun design.
- Healthcheck endpoint (/healthcheck.json).

---

## Configuration

See the [wiki](https://github.com/chrede88/qubt/wiki) for all info about configuration.

---

## Update the Theme Version
The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/chrede88/qubt@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. You can find the releases [here](https://github.com/chrede88/qubt/releases). Please check if any breaking changes are listed under the release you want to update to, before proceeding.