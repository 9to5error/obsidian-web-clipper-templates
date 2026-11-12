```json
{
	"schemaVersion": "0.1.0",
	"name": "YouTube (iOS) - English Version",
	"behavior": "create",
	"noteContentFormat": "> **Source:** [{{author}}]({{meta:property:og:url}})\n> **Clipped on:** {{date|date:\"YYYY-MM-DD\"}}T{{date|date:\"HH:mm:ss\"}}+07:00\n\n---\n\n## Video\n\n![]({{meta:property:og:url}})\n\n[If the player does not appear, open it on YouTube]({{meta:property:og:url}})\n\n---\n\n## Summary 🤖\n\n{{\"Read ONLY the video description in the context, not the rest of the page. Write a technical summary in English as 3 sections using H3 headings (###), with no H2 title: 1) Prerequisites / Tools needed, 2) Core steps in order, 3) Tips & Troubleshooting. Do not use information from viewer comments, related videos, or the sidebar; if a section is not covered in the description, write 'Not stated in the video description'. Keep tool names, terminal commands, and links exactly as written. Do not invent steps or numbers.\"}}\n",
	"properties": [
		{
			"name": "created",
			"value": "{{date|date:\"YYYY-MM-DD\"}}",
			"type": "date"
		},
		{
			"name": "tags",
			"value": "youtube",
			"type": "multitext"
		},
		{
			"name": "source",
			"value": "{{meta:property:og:url}}",
			"type": "text"
		},
		{
			"name": "channel",
			"value": "{{author}}",
			"type": "text"
		}
	],
	"context": "TITLE: {{title}}\n\nVIDEO DESCRIPTION:\n{{meta:property:og:description}}",
	"triggers": [
		"https://m.youtube.com/watch",
		"https://m.youtube.com/shorts/",
		"https://m.youtube.com/live/"
	],
	"noteNameFormat": "{{title|replace:\" - YouTube\":\"\"|safe_name|trim}}",
	"path": "Clippings/Youtube"
}
```
