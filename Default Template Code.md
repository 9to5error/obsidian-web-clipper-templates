```json
{
	"schemaVersion": "0.1.0",
	"name": "Default - English Version",
	"behavior": "create",
	"noteContentFormat": "> [!info] Source\n> [{{domain}}]({{url}})\n> Clipped: {{date|date:\"YYYY-MM-DD\"}}\n\n---\n\n## Summary\n\n{{\"Read this page, then write a summary in plain, compact English. Two paragraphs, 8-12 sentences total. First paragraph: what this page is about, who it is for, and what problem it answers. Second paragraph: the main ideas, core arguments, or conclusions the author makes. Use ONLY information that is actually on the page. Do not invent numbers, tool names, steps, or conclusions. Do not use Markdown headings, lists, or bullets. Do not use the # symbol. No opening sentence such as 'Here is a summary'.\"}}\n\n---\n\n## Key Points\n\n{{\"Take the 6-10 most important points from this page, in page order. Each point is one compact sentence (maximum 25 words), starting with a dash and a space. One level of sub-bullets is allowed when a point has details. Keep technical terms and product names exactly as written. Do not put the # symbol in front of a term; write the name without it. Use ONLY what is on the page; if the content is thin, write fewer points. Do not use headings. No opening or closing sentence.\"}}\n\n---\n\n## Key Terms\n\n{{\"Take 3-6 important terms, concepts, or abbreviations from this page that a reader should know. Format each line as: dash, space, the term in bold, space, an em dash, then a one-sentence explanation. Write the explanation in English. Do not put the # symbol in front of a term; write the name without it. If the page has no special terms, write only a dash. Do not use headings. No opening sentence.\"}}\n\n---\n\n## Full Content\n\n{{content|replace:\"/!\\[[^\\]]*\\]\\(data:image[^)]*\\)/g\":\"\"|replace:\"/(\\[?!\\[[^\\]]*\\]\\([^)]*\\)\\]?(?:\\([^)]*\\))?)/g\":\"\\n\\n$1\\n\\n\"|replace:\"/([^\\w\\\\&\\n`])(?<!\\]\\()#([A-Za-z][\\w-]*)/g\":\"$1`#$2`\"}}\n",
	"properties": [
		{
			"name": "created",
			"value": "{{date|date:\"YYYY-MM-DD\"}}",
			"type": "date"
		},
		{
			"name": "tags",
			"value": "clippings",
			"type": "multitext"
		},
		{
			"name": "source",
			"value": "{{url}}",
			"type": "text"
		},
		{
			"name": "author",
			"value": "{{author}}",
			"type": "text"
		},
		{
			"name": "title",
			"value": "{{title|replace:\" - Google Search\":\"\"|trim}}",
			"type": "text"
		},
		{
			"name": "description",
			"value": "{{description}}",
			"type": "text"
		}
	],
	"context": "{{content}}",
	"triggers": [],
	"noteNameFormat": "{{title|replace:\" - Google Search\":\"\"|safe_name|trim}}",
	"path": "Clippings/Default"
}
```
