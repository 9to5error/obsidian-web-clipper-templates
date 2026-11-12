```json
{
	"schemaVersion": "0.1.0",
	"name": "YouTube (Desktop) - English Version",
	"behavior": "create",
	"noteContentFormat": "\n> **Source:** [{{author}}](https://youtu.be/{{url|replace:\"/.*v=([^&]+).*/\":\"$1\"}})\n> **Clipped on:** {{date}}\n\n---\n\n## Video\n\n![Video|640x360](https://www.youtube.com/watch?v={{url|replace:\"/.*v=([^&]+).*/\":\"$1\"}}#t=0)\n\n---\n\n## Summary 🤖\n{{\"Summarize this video in English using ONLY the description on this page. If the description is short, write one paragraph plus 2-4 bullets that are actually present in it. Do NOT invent steps, numbers, or tool names that are not mentioned. If the information is thin, end with one sentence: Technical details are not in the description; check the transcript.\"}}\n\n---\n\n## Key Points ⏱️\n\n{{\"Turn the transcript in the context into a compact English summary. Write 10-15 points in video order, one short sentence each. Every point MUST start with a Markdown time link: [M:SS](https://youtu.be/VIDEO_ID?t=SECONDS), where VIDEO_ID is copied exactly from the VIDEO_ID line in the context, and SECONDS equals minutes times 60 plus seconds from the original transcript timestamp. Use only timestamps that actually appear in the transcript. Do not invent moments, numbers, or tool names. Keep product names and technical terms as written. No intro or closing sentence.\"}}\n\n---\n\n## Description\n\n{{\"Keep the video description on this page in English. Preserve line structure, lists, links, timestamps, product names, and technical terms exactly as they are. Do not add or remove content, do not add commentary.\"}}\n\n---\n\n## Transcript (reference)\n\n> [!quote]- Original transcript (auto-caption) - expand only to verify what was actually said\n{{transcript|blockquote}}\n",
	"properties": [
		{ "name": "created", "value": "{{date|date:\"YYYY-MM-DD\"}}", "type": "date" },
		{ "name": "tags", "value": "youtube", "type": "multitext" },
		{ "name": "source", "value": "https://youtu.be/{{url|replace:\"/.*v=([^&]+).*/\":\"$1\"}}", "type": "text" },
		{ "name": "channel", "value": "{{author}}", "type": "text" }
	],
	"context": "VIDEO_ID: {{url|replace:\"/.*v=([^&]+).*/\":\"$1\"}}\nURL: {{url}}\n\n{{content}}\n\n{{transcript}}",
	"triggers": ["https://www.youtube.com/watch"],
	"noteNameFormat": "{{meta:property:og:title|replace:\" - YouTube\":\"\"|safe_name|trim}}",
	"path": "Clippings/Youtube"
}
```
