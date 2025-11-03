# N8N-automation-for-news
This N8N workflow uses rss feed from news sites to provide summarized news on a discord channel.
DISCORD FOR NEWS
Overview
This n8n automation named DISCORD FOR NEWS reads news from an RSS feed (https://www.cbsnews.com/latest/rss/world) and limits the number of news items processed to 5. It uses a language model chain connected to an Ollama chat model to summarize news content in a small paragraph. Finally, it sends the summarized news to a specified Discord channel via a webhook. The workflow can be triggered on a schedule, but the schedule trigger is disabled by default.

Workflow Details
Schedule Trigger: Disabled by default; can be enabled to automate the workflow at desired intervals.

RSS Read: Fetches latest world news from CBS News RSS feed.

Limit: Limits processing to 5 news items per run to control load.

Basic LLM Chain: Uses a language model to generate a concise summary from the news content.

Ollama Chat Model: Provides the language model backend (llama3.2:1b) for the summarization.

Discord: Sends the summarized text to a Discord channel using a webhook for real-time news updates.

Setup Instructions
Configure the Discord Webhook credentials in the Discord node.

Enable and configure the Schedule Trigger node according to preferred intervals to automate.

Test the workflow to verify summary posts are sent to your Discord channel.

Adjust the RSS feed URL if you want news from different sources or categories.

Modify the max items parameter in the Limit node to control the number of summaries per run.

Notes
The Schedule Trigger node is disabled by default.

The automation processes up to 5 news items per run.

Summaries are generated using a prompt instructing the model to create a short paragraph without further questions.

