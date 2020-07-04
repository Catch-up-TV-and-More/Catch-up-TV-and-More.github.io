# Catch-up TV & More website

This repository contains [Catch-up TV & More official website](https://catch-up-tv-and-more.github.io) on `master` branch and Jekyll source files allowing of build the website on `jekyll-source` branch.

## How to modify the website

1. Install Bundler and Jekyll on your local machine

```
gem install bundler jekyll
```

2. Clone this repository and move into `jekyll-source` branch

```
git clone https://github.com/Catch-up-TV-and-More/Catch-up-TV-and-More.github.io
git checkout jekyll-source
```

3. Install dependences

```
bundle install
```

4. Modify whatever you want

5. Make the website available on a local server to check your changes on http://127.0.0.1:4000/

```
bundle exec jekyll serve
```

7. Once everything is ok for you, push your changes

```
git add --all
git commit -m "Update Website"
git push
```

8. Wait a little so that a GitHub action workflow will build the website on [https://catch-up-tv-and-more.github.io](https://catch-up-tv-and-more.github.io)

## Notes

* Do not push anything on `master` branch because the GitHub action workflow that build the website from `jekyll-source` branch perform a `push force` on master branch
* The GitHub action workflow that build the website is triggered on each `push` on `jekyll-source` branch
