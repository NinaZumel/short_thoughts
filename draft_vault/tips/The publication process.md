
Micro.blog effectively has a 300 character limit.

1. Write post. Use the obsidian `short thoughts template 11ty` template to format the date correctly. I've been giving the markup files a title `yyyy-mm-dd-descriptive-title`. The new version of the blog will take a `title`, too, for super long posts.

2. Copy the post into the `contents/blog` folder of the local blog repo. Any images go into `../content/blog/images`.
```
mv [filename].md ../content/blog
cd ../  # this should be short_thoughts root
```

4.  then in `short_thoughts` directory:
```
git add .
git commit
git push

npm run build # (or build-ghpages, they're the same here)
npm run deploy
```

4. Go to Github -> short_thoughts -> pages and check for when the site updates. The actions tab will tell you when

4. Once the site has updated, send a ping to Micro.blog

```
curl -X POST -F 'url=https://ninazumel.com/short_thoughts/feed.xml' https://micro.blog/ping
```

e.g. 
> curl -X POST -F 'url=https://YOUR-FEED-URL-HERE' https://micro.blog/ping  

#tips

