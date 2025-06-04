+++
title = 'Posting'
date = 2025-06-04T12:16:36-07:00
draft = false
+++

Git pull from the root of the www repo.

Run `hugo new content content/post/my-post.md` from the root directory of the hugo repo. 

Copy words as markdown from google doc into markdown doc.

Make a new folder called the name of the post in `/static/img/post` and place all images there including the thumbnail.

Add all image references to the markdown document. The thumbnail is simply an image reference at the top of the page. 

The image reference path in markdown follows this pattern `/img/post/post-folder/img.png` . 

Markdown image syntax `![alt text](path)`. 

Markdown link syntax `[text](https://link)`.

Run this command in the /static/img folder that you created to compress all of the pngs *this command only works for pngs*   
`find . -iname '*.png' -exec pngquant --quality=10 --ext .png --force {} \;` 

Set draft to false in the markdown file and run `hugo serve` from the root of the www repo and check formatting.
