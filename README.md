# OpenTechSchool Materials Landing

A simple one-page landing for all of OTS' workshop materials.

Built using the [Gumby Framework](http://gumbyframework.com).

You can edit / add the workshop materials simply by editing the yaml
`sections` dictionary found in `_config.yml`.

To build this site, you'll need Ruby installed, and possibly Node.js.

### Ruby

Use `bundle install`, or install the `compass`, `jekyll` and
`modular-scale` gems.

To run the site, use `compass watch` in one terminal and `jekyll serve -w` in
another, then visit http://localhost:4000/

CSS adjustments are made in `sass/_custom.scss` and `sass/_fonts.scss`.

Jekyll might not automatically rebuild the site if you have changed
`_config.yml`, so I just `rm -rf _site/*` before restarting the server again.

The `gh-pages` branch is committed to from the generated `_site/` folder.

### Node.js

Only needed to update gumby.

Node requirements: `bower`, `claymate`. These two are designed to be installed
globally (`npm install -g bower claymate`).

To update gumby, use `bower update gumby`. To then rebuild it, use
`claymate build`.

### Updating the repo

In order to push to gh-pages for the first time:

1. `rm -rf _site`
2. `mkdir _site; cd _site`
3. `git clone -b gh-pages git@github.com:OpenTechSchool/learn.opentechschool.org.git .`
4. `cd ../; compass compile; jekyll build`
5. `cd _site; git commit -a`
6. Commit and push.
