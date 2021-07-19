# We Need to Talk

## Adding an article

To add an article, make an article file titled <YYYY-MM-DD-article-nickname>.md in the `_posts` directory. This markdown file will hold some frontmatter (denoted by the three dashes at the top of the document) and some markdown/HTML. The frontmatter contains variables that will be used throughout the site to render the article correctly. Required variables are:

* title
* layout (this should always be set to *post*)
* author
* cover_photo (provide a path to the article cover photo in the assets/images folder)
* section 

Optional variables are:

* tw (contains text to appear below the article title as a trigger warning)
* tags (if you tag a post as "featured", it will appear in the Featured sidetab)

I **highly** recommend using one of the existing posts as an example. For a post with lots of images, try `_posts/2021-06-27-beauty-standards.md`. For a post with a trigger warning, try `_posts/2021-06-27-how-feminism-is.md`

### Adding article photos

If you want to add photos to an article, you need to add it to the frontmatter and then add it to the article body. To add the Nth photo to an article, add to the frontmatter:

* photoN (path to photo in the assets/images folder)
* captionN (optional image caption)

Add to the article text markdown the following block of HTML, replacing N with the actual number of the photo as specified in the frontmatter

```
<div class="pr-0 justify-content-center ">
    <figure>
	    <img class="rounded img-fluid" src="{% if page.photoN contains "://" %}{{ page.photoN }}{% else %}{{ site.baseurl }}/{{ page.photoN }}{% endif %}" alt="{{ page.title }}">
        {% if page.captionN %}
            <figcaption class="figure-caption">{{page.captionN}}</figcaption>
        {% endif %}
    </figure>
</div>
```



## Adding an edition

To add an edition, add a markdown file titled "<month><year>.md" to the `_editions` directory. In the frontmatter, specify the cover photo file name, the pdf file name, and the date. See `oct2020.md` as an example. Upload the cover photo in `assets/images` and the pdf file in `assets/editions`

## FAQ

**Why is my edition cover photo too small?**

In order for edition cover photos to display well on all browsers and monitors, the images need to be sufficiently large. Try uploading an edition cover photo with a larger size.
