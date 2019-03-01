# Blog Channel Set

The Blog Channel Set comes with custom fields, statuses, and categories to get your blog up and running fast. Here’s what’s inside:

### Custom Fields

* `{blog_content}`: a Textarea for the blog post’s content
* `{blog_image}`: a File field for a featured image for the blog post

### Statuses

* Open: published
* Closed: not published
* Featured: to call attention to a blog post, typically on the homepage

### Categories

* News
* Personal
* Photos
* Videos
* Music

### Sample Tags

```
{exp:channel:entries channel='blog' limit='1' require_entry='yes'}
	{if no_results}
		{redirect='404'}
	{/if}

	<h1>Blog Channel Set</h1>

	{if has_categories}
		<div>Categories:
			<ul>
				{categories}
					<li><a href="{path='blog/index'}">{category_name}</a></li>
				{/categories}
			</ul>
		</div>
	{/if}

	{if blog_image}
		{blog_image}
			<figure>
				<img src="{blog_image:image}" alt="{blog_image:caption}">
				<figcaption>{blog_image:caption}</figcaption>
			</figure>
		{/blog_image}
	{/if}

	{blog_content}
{/exp:channel:entries}
```

## License

Copyright (C) 2004 - 2016 EllisLab, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL ELLISLAB, INC. BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Except as contained in this notice, the name of EllisLab, Inc. shall not be used in advertising or otherwise to promote the sale, use or other dealings in this Software without prior written authorization from EllisLab, Inc.
