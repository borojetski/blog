This is an 11ty site forked ([httpsterio](https://github.com/httpsterio/11ty-blog-njk-starter)) from a fork ([kohrongying](https://github.com/kohrongying/11ty-blog-starter)).

## Features
- Static Site Gen - Eleventy

- Tailwind CSS v2.0 / Tailwind Typography / Dark Mode

- Create excerpts using the `<!-- excerpt -->`

- Custom ReadTime filter

- 404 page

+ Tags page to view posts related to tag
  - Use of a `tagList` collection defined in `.eleventy.js`
  - `/tags` - show all available tags (excluding all and posts) as buttons (`tags.md`)
  - `/tags/tag-name` - shows all posts related to that tag (`tagList.md`)

+ Sitemap and Robots.txt 
  - Change site url in `_data/site.json`

+ Shortcode to handle images
  - Add image under `src/assets/img/posts` and use the asset_img short code
  - `{% asset_img 'filename', 'alt_text' %}` eg. `{% asset_img 'mailbox.jpg', 'picture of a mailbox' %}`
  - You can provide an optional third argument for the image folder path if your image isn't inside `src/assets/img/posts`
  - eg. `{% asset_img 'mailbox.jpg', 'picture of a mailbox', '/images/' ` 
  - the comma between argument's is __not__ optional

- Draft posts using the `published` frontmatter

+ Posts pagination in `index.html` 
  - change the `size` frontmatter variable

- ESLint

+ Bash script to create new post (based on YYYY and MM)
```bash
$ ./create new blog post
Created new post at src/posts/2021/01/new-blog-post.md
```

## Running locally

Create your posts under `src/posts`.

Navigate to localhost:8080 after starting the server.
```
npm start
```

On Cloudflare Pages / Netlify / Surge / Firebase hosting / etc hosting providers

Build Command: `npm run build`

Output folder: `_site`

## Future Improvemeents

- [ ] Make next/prev posts