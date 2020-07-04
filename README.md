# Catch-up TV & More Jekyll website sources

This repository contains the Jekyll project allowing to build the [Catch-up TV & More official website](https://catch-up-tv-and-more.github.io).

## How to modify the website

1. Install Bundler and Jekyll

```
gem install bundler jekyll
```

2. Clone the repositories

```
git clone https://github.com/Catch-up-TV-and-More/Catch-up-TV-and-More.github.io
git clone https://github.com/Catch-up-TV-and-More/jekyll-website
```

3. Install dependences

```
cd jekyll-website
bundle install
```

4. Modify wathever you want in jekyll-website

5. Make it available on a local server

```
bundle exec jekyll serve -d ../Catch-up-TV-and-More.github.io
```

6. Check the new website locally on http://127.0.0.1:4000/

7. Once the website is correct you need to build it

```
bundle exec jekyll build -d ../Catch-up-TV-and-More.github.io
```

7. Push modifications on GitHub Pages

```
cd ../Catch-up-TV-and-More.github.io
git add --all
git commit -m "Update Website"
git push
```

8. Wait a minute and check your modifications on [https://catch-up-tv-and-more.github.io](https://catch-up-tv-and-more.github.io)

