# reddit-short-stories
4308 short stories (4 million words) scraped from https://reddit.com/r/WritingPrompts

Scraped and formatted by Trevor Du (me!)

## Dataset description
* Each line of [reddit_short_stories.txt](../https://github.com/tdude92/reddit-short-stories/blob/master/reddit_short_stories.txt) is one full short story.
* Each short story begins with an "\<sos>" token and ends with an "\<eos>" token (eg. "\<sos> once upon a time, the end \<eos>").
* Newline characters in a story are replaced with the "\<nl>" token (eg. "\<sos> line 1\ <nl> line 2 \<eos>")

## Data Collection Method
r/WritingPrompts is a forum on the popular discussion website, https://reddit.com. The tradition is that users start threads that are titled with a *Writing Prompt*. In these threads, other users comment a short story they've written based on the original prompt.

The scraper saved a comment on a post on r/WritingPrompts if the following conditions are satisfied:
* The post is flaired "Writing Prompt"
* The post has >=1.0k upvotes.
* The author of the comment is not a moderator of r/WritingPrompts (to avoid scraping automod posts and mod announcements).
* The comment has >=200 upvotes.
* The comment has >=200 words.
* <20 comments have already been scraped from the comment's parent post.

Note: Only a portion of r/WritingPrompts was scraped, not the entire thing.