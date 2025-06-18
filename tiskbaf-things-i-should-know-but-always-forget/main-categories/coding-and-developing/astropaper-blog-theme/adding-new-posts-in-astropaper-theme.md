# Adding new posts in AstroPaper theme

### Frontmatter[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#frontmatter) <a href="#frontmatter" id="frontmatter"></a>

Frontmatter is the main place to store some important information about the blog post (article). Frontmatter lies at the top of the article and is written in YAML format. Read more about frontmatter and its usage in [astro documentation](https://docs.astro.build/en/guides/markdown-content/).

Here is the list of frontmatter property for each post.

| Property           | Description                                                                                 | Remark                                        |
| ------------------ | ------------------------------------------------------------------------------------------- | --------------------------------------------- |
| _**title**_        | Title of the post. (h1)                                                                     | required\*                                    |
| _**description**_  | Description of the post. Used in post excerpt and site description of the post.             | required\*                                    |
| _**pubDatetime**_  | Published datetime in ISO 8601 format.                                                      | required\*                                    |
| _**modDatetime**_  | Modified datetime in ISO 8601 format. (only add this property when a blog post is modified) | optional                                      |
| _**author**_       | Author of the post.                                                                         | default = SITE.author                         |
| _**slug**_         | Slug for the post. This field is optional but cannot be an empty string. (slug: ""❌)        | default = slugified file name                 |
| _**featured**_     | Whether or not display this post in featured section of home page                           | default = false                               |
| _**draft**_        | Mark this post ‘unpublished’.                                                               | default = false                               |
| _**tags**_         | Related keywords for this post. Written in array yaml format.                               | default = others                              |
| _**ogImage**_      | OG image of the post. Useful for social media sharing and SEO.                              | default = SITE.ogImage or generated OG image  |
| _**canonicalURL**_ | Canonical URL (absolute), in case the article already exists on other source.               | default = `Astro.site` + `Astro.url.pathname` |

> Tip! You can get ISO 8601 datetime by running `new Date().toISOString()` in the console. Make sure you remove quotes though.

Only `title`, `description` and `pubDatetime` fields in frontmatter must be specified.

Title and description (excerpt) are important for search engine optimization (SEO) and thus AstroPaper encourages to include these in blog posts.

`slug` is the unique identifier of the url. Thus, `slug` must be unique and different from other posts. The whitespace of `slug` should to be separated with `-` or `_` but `-` is recommended. Slug is automatically generated using the blog post file name. However, you can define your `slug` as a frontmatter in your blog post.

For example, if the blog file name is `adding-new-post.md` and you don’t specify the slug in your frontmatter, Astro will automatically create a slug for the blog post using the file name. Thus, the slug will be `adding-new-post`. But if you specify the `slug` in the frontmatter, this will override the default slug. You can read more about this in [Astro Docs](https://docs.astro.build/en/guides/content-collections/#defining-custom-slugs).

If you omit `tags` in a blog post (in other words, if no tag is specified), the default tag `others` will be used as a tag for that post. You can set the default tag in the `/src/content/config.ts` file.

```
// src/content/config.ts
export const blogSchema = z.object({
  // ---
  draft: z.boolean().optional(),
  tags: z.array(z.string()).default(["others"]), // replace "others" with whatever you want
  // ---
});
Copy
```

#### Sample Frontmatter[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#sample-frontmatter) <a href="#sample-frontmatter" id="sample-frontmatter"></a>

Here is the sample frontmatter for a post.

```
# src/content/blog/sample-post.md
---
title: The title of the post
author: your name
pubDatetime: 2022-09-21T05:17:19Z
slug: the-title-of-the-post
featured: true
draft: false
tags:
  - some
  - example
  - tags
ogImage: ""
description: This is the example description of the example post.
canonicalURL: https://example.org/my-article-was-already-posted-here
---
Copy
```

### Adding table of contents[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#adding-table-of-contents) <a href="#adding-table-of-contents" id="adding-table-of-contents"></a>

By default, a post (article) does not include any table of contents (toc). To include toc, you have to specify it in a specific way.

Write `Table of contents` in h2 format (## in markdown) and place it where you want it to be appeared on the post.

For instance, if you want to place your table of contents just under the intro paragraph (like I usually do), you can do that in the following way.

```
---
# some frontmatter
---

Here are some recommendations, tips & ticks for creating new posts in AstroPaper blog theme.

## Table of contents

<!-- the rest of the post -->
Copy
```

### Headings[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#headings) <a href="#headings" id="headings"></a>

There’s one thing to note about headings. The AstroPaper blog posts use title (title in the frontmatter) as the main heading of the post. Therefore, the rest of the heading in the post should be using h2 \~ h6.

This rule is not mandatory, but highly recommended for visual, accessibility and SEO purposes.

### Storing Images for Blog Content[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#storing-images-for-blog-content) <a href="#storing-images-for-blog-content" id="storing-images-for-blog-content"></a>

Here are two methods for storing images and displaying them inside a markdown file.

> Note! If it’s a requirement to style optimized images in markdown you should [use MDX](https://docs.astro.build/en/guides/images/#images-in-mdx-files).

#### Inside `src/assets/` directory (recommended)[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#inside-srcassets-directory-recommended) <a href="#inside-srcassets-directory-recommended" id="inside-srcassets-directory-recommended"></a>

You can store images inside `src/assets/` directory. These images will be automatically optimized by Astro through [Image Service API](https://docs.astro.build/en/reference/image-service-reference/).

You can use relative path or alias path (`@assets/`) to serve these images.

Example: Suppose you want to display `example.jpg` whose path is `/src/assets/images/example.jpg`.

```
![something](@assets/images/example.jpg)

<!-- OR -->

![something](../../assets/images/example.jpg)

<!-- Using img tag or Image component won't work ❌ -->
<img src="@assets/images/example.jpg" alt="something">
<!-- ^^ This is wrong -->
Copy
```

> Technically, you can store images inside any directory under `src`. In here, `src/assets` is just a recommendation.

#### Inside `public` directory[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#inside-public-directory) <a href="#inside-public-directory" id="inside-public-directory"></a>

You can store images inside the `public` directory. Keep in mind that images stored in the `public` directory remain untouched by Astro, meaning they will be unoptimized and you need to handle image optimization by yourself.

For these images, you should use an absolute path; and these images can be displayed using [markdown annotation](https://www.markdownguide.org/basic-syntax/#images-1) or [HTML img tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img).

Example: Assume `example.jpg` is located at `/public/assets/images/example.jpg`.

```
![something](/assets/images/example.jpg)

<!-- OR -->

<img src="/assets/images/example.jpg" alt="something">
Copy
```

### Bonus[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#bonus) <a href="#bonus" id="bonus"></a>

#### Image compression[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#image-compression) <a href="#image-compression" id="image-compression"></a>

When you put images in the blog post (especially for images under `public` directory), it is recommended that the image is compressed. This will affect the overall performance of the website.

My recommendation for image compression sites.

* [TinyPng](https://tinypng.com/)
* [TinyJPG](https://tinyjpg.com/)

#### OG Image[#](https://musings-of-an-adhd-tech-geek.vercel.app/posts/adding-new-posts-in-astropaper-theme/#og-image) <a href="#og-image" id="og-image"></a>

The default OG image will be placed if a post does not specify the OG image. Though not required, OG image related to the post should be specify in the frontmatter. The recommended size for OG image is _**1200 X 640**_ px.
