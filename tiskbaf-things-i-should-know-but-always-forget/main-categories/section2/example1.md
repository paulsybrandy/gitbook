---
description: >-
  A quick and relatively easy way to display just about any RSS feed on a page
  within your Notion.
---

# RSS Feed in your Notion Pages

⚠️NOTE: 👨‍💻 Source code is [available here](https://github.com/antoinechalifour/notion-embed-rss).

***

### **How to use this Widget (Steps)**

1. Gather all the RSS feeds URLs ;
2. Replace the **\[COMA\_SEPARATED\_SOURCES]** section of the following URL with the concatenated feeds URLs (coma-separated) ;
   * (Option) Tell the widget how many days since the articles have been published (defaults to 14)

```
<https://notion-widget-rss.vercel.app/?sources=**[COMA_SEPARATED_SOURCES]**&sinceDays=**[NUMBER]**>
```

3. Create an _Embed_ block and paste the URL generated in step 2.

{% embed url="https://file.notion.so/f/f/9f6a7a04-d71f-4fd7-8d86-ceddfacf42a3/452604e5-df89-42b6-9d5e-7fb0d92778dc/Untitled.png?downloadName=Untitled.png&expirationTimestamp=1721160000000&id=8b451e59-4869-48c7-a614-9125ac2bcf51&signature=YrmMISYW0L37U6164V9mfk3PAHV9xQIzzE_K_D3P83I&spaceId=9f6a7a04-d71f-4fd7-8d86-ceddfacf42a3&table=block" %}
Creating an embed block in Notion
{% endembed %}

4. You're done!

***

[**Customize** ](https://file.notion.so/f/f/9f6a7a04-d71f-4fd7-8d86-ceddfacf42a3/452604e5-df89-42b6-9d5e-7fb0d92778dc/Untitled.png?id=8b451e59-4869-48c7-a614-9125ac2bcf51\&table=block\&spaceId=9f6a7a04-d71f-4fd7-8d86-ceddfacf42a3\&expirationTimestamp=1721160000000\&signature=YrmMISYW0L37U6164V9mfk3PAHV9xQIzzE\_K\_D3P83I\&downloadName=Untitled.png)

This widget is customizable so that it can match your Notion pages theme. You use the following `query` params to customise :

* The _font_:
  * mono: `&font=mono` ;
  * serif: `&font=serif` ;
  * default (sans-serif): `&font=default`
* The _theme:_
  * light: `&theme=light` ;
  * dark: `&theme=dark`

_Examples :_

**Serif with Light Theme**

```
<https://notion-widget-rss.vercel.app/?**font=serif&theme=light&**sources=https://www.reddit.com/r/webdev.rss>
```

[https://notion-widget-rss.vercel.app/?sources=https://www.reddit.com/r/webdev.rss\&font=serif\&theme=light](https://notion-widget-rss.vercel.app/?sources=https://www.reddit.com/r/webdev.rss\&font=serif\&theme=light)

**Mono with Dark Theme**

```
<https://notion-widget-rss.vercel.app/?**font=mono&theme=dark&**sources=https://www.reddit.com/r/webdev.rss>
```

[https://notion-widget-rss.vercel.app/?sources=https://www.reddit.com/r/webdev.rss\&font=mono\&theme=dark](https://notion-widget-rss.vercel.app/?sources=https://www.reddit.com/r/webdev.rss\&font=mono\&theme=dark)

***

\<aside> 💅 **Troubleshooting**

\</aside>

⛔️ **Invalid source or feed**

In the example bellow, [**http://example.com**](http://example.com) and [\*\*](http://localhost/feed)[http://localhost/feed\*\*](http://localhost/feed\*\*) are invalid sources.

[https://notion-widget-rss.vercel.app/?sources=http://example.com,http://localhost/feed,https://www.reddit.com/r/webdev.rss\&font=mono](https://notion-widget-rss.vercel.app/?sources=http://example.com,http://localhost/feed,https://www.reddit.com/r/webdev.rss\&font=mono)

If the widget cannot fetch or parse the RSS feed, an error message will be displayed in place. To fix it, verify the source or remove it.If you're sure the URL and the RSS feed is valid, please [file an issue on the Github repository](https://github.com/antoinechalifour/notion-embed-rss/issues).
