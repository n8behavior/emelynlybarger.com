# Emelyn Lybarger Website

View test site at

https://n8behavior.github.io/emelyn-lybarger-website/

## Publishing

Easest to run the `.publish` script.

```
.publish
```

This will abort if there are errors or pending changes in the working directory and also makes sure that all previously existing output files are removed.

## Manual Publishing

To publish to the GitHub pages project site do the followinging from `main` branch.  Note, my remote is called `gh`, yours might be called `origin`, so adjust the `git push ...` below as-needed.

### Setup for building

Make sure you have the `gh-pages` branch checked out into `public/` using `git worktree`

```
rm -rf public
git worktree add -B gh-pages public gh/gh-pages
```

### Build

```
hugo
```

### Publish

If that works, then publish the site.

```
cd public
git add --all
git commit -m "Publishing to gh-pages"
cd -
git push gh gh-gages
```
