```json
{
	"schemaVersion": "0.1.0",
	"name": "Reddit Post - English Version",
	"behavior": "create",
	"noteContentFormat": "> [!info] Source\n> [{{selector:shreddit-post?subreddit-prefixed-name}}]({{url}}) on Reddit\n> Posted by u/{{author}}\n> Clipped: {{date|date:\"YYYY-MM-DD\"}}\n\n---\n\n## Discussion Consensus 🤖\n\n{{\"Read the Reddit thread in the context, including its comments. Write in English using two H3 headings (###) with no H2 title: 1) Thread Summary — the main topic, or the question OP asked, in 2-3 sentences. 2) Solutions & Comment Highlights — 3-5 points from the most upvoted comments, one sentence each, naming the username where it matters. Use ONLY what the thread and its comments actually contain. Do not invent quotes, upvote counts, or usernames. Do not conclude anything the thread does not discuss. No opening or closing sentence.\"}}\n\n---\n\n## Post Content\n\n{{content}}\n",
	"properties": [
		{
			"name": "title",
			"value": "{{selector:shreddit-post?post-title|trim}}",
			"type": "text"
		},
		{
			"name": "created",
			"value": "{{date|date:\"YYYY-MM-DD\"}}",
			"type": "date"
		},
		{
			"name": "url",
			"value": "{{url}}",
			"type": "text"
		},
		{
			"name": "tags",
			"value": "source/reddit",
			"type": "multitext"
		},
		{
			"name": "published",
			"value": "{{selector:shreddit-post?created-timestamp|date:\"YYYY-MM-DD\"}}",
			"type": "date"
		},
		{
			"name": "subreddit",
			"value": "{{selector:shreddit-post?subreddit-prefixed-name}}",
			"type": "text"
		}
	],
	"triggers": [
		"https://www.reddit.com"
	],
	"noteNameFormat": "{{selector:shreddit-post?post-title|trim|safe_name}}",
	"path": "Clippings/Reddit"
}
```
