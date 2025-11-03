DISCORD FOR NEWS
Overview
This n8n automation streams the latest world news from CBS News RSS feed, summarizes the content using a powerful language model, and posts concise news updates directly to a Discord channel via webhook. It enables real-time news delivery in Discord servers with automated summarization of complex news articles into brief paragraphs.

##How It Works##

Fetches news from the RSS feed: https://www.cbsnews.com/latest/rss/world.

Limits to the top 5 news articles to keep messages concise and manageable.

Summarizes each article into a small paragraph using a connected language model (llama3.2:1b via Ollama).

Sends the generated summaries to a specified Discord channel using a webhook integration.

##Features##

Discord webhook integration: Seamless posting of summaries into Discord chats.

AI-powered summarization: Uses an LLM chain with Ollama chat model to condense news content.

Configurable schedule trigger: Automate news fetching and posting at preferred intervals (disabled by default).

Item limit control: Manage how many news pieces get posted per run for channel clarity.

##Setup Instructions##

Create a Discord webhook URL for the channel you want to post the news in.

Configure the Discord node in n8n with your webhook credentials.

(Optional) Enable and schedule the trigger node to automate news updates.

Run the workflow manually to verify messages appear in Discord.

Customize the RSS feed or summary prompt as needed.

##Usage Tips for Discord##

Adjust the summary prompt to match your Discord community’s tone — concise, formal, or casual.

Set an appropriate schedule to avoid flooding the channel with too many updates.

Use Discord message formatting (Markdown) if you want enhanced readability.

Consider adding additional nodes for filtering or enriching news before posting to Discord.

##Notes##

The schedule trigger node is disabled by default; enable it to automate.

The automation currently processes up to 5 news items each execution.

Summary generation is designed to produce brief, clear paragraphs without unnecessary questions.
