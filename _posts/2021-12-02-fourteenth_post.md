---
layout: post
title: Pushing Internal Data To Repo: An Anecdote
---

Wanted to tell a quick story of one of the close calls I had working in Security this year. 
A lot of times people only talk about their highlights or their accomplishments. But it is a good 
exercise to learn from our mistakes.

I have a running list of notes I keep on my work laptop. Think things like definitions to different tools, short code snippets, and more that I can use regardless of the setting. One day I was working on github and I pushed this file. This normally wouldn’t be an issue if there is no internal data within it, after all it's just general notes.

The problem was there was an internal webhook in the file. Webhooks are “always on" listeners that will deliver data when a specified action occurs. Think of a Typeform or Slack notification. A couple days later I was notified of this problem, and I double checked the github push. Sure enough there was the webhook. We start an incident and remediation starts. 


![Github Push Meme](/images/github_push.jpeg)
<br>

Due to the way github works, simply removing this file is not good enough from a security and privacy standpoint, as the 
secret will remain in git history. I ended up using the git-filter repo tool to address this.
[Removing Sensitive Data From A Repository](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#using-git-filter-repo)
<br>


What this tool does is remove the specified file, any commits referencing it, and rewrite history. 
Making it seem as if the mistake never happened. I was able to fix the incident and learn how to use a new tool. 

I like to go by the adage of “I either win or I learn”, and this was definitely a learning experience.
I think we can all take some time and remember moments where we really learned through adverse 
experiences and came out better because of it. 


