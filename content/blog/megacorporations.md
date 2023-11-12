+++
title = 'Only Trust The Things You make'
date = 2023-11-08T00:05:04-07:00
tags = ["blog"]
+++
### Introduction
This was inspired by a little incident I had today where Google Docs wasn't properly emailing people about comment tags and assignments.

This is a piece about minimalism, dependence and trust.

#### Background
My dad has always told me that he would always trust a massive company more than a smaller one no matter what he is doing. He says it's because the larger companies have more money and that if they break the law or something goes wrong, then he can just sue them for money. 

Well, obviously this isn't true when they are already breaking the law and treating fines as another expense, getting hacked and leaking customer data with no repercussions, leaving CVEs unfixed or just the fact that no individual is going to sue them unless that person lost their life savings or something like that.

Assuming it is true though, this is my response.

### Separator 
Let's take the example I have in the Introduction. Google Docs breaks. I have a time sensitive project I have to work on. We don't get any work done for a few days. What now? Can I sue Google? No. I can blame them, but what is that going to fix. How will I be compensated? I just can't for something like this. 

Lets say that I had built a system similar to Google Docs. The same breakage happens with my project. Now what? I can blame myself. That might not be that much of a difference, but I can change it. I control what happens, so if it breaks I get to fix it, if I don't fix it I suffer the same consequences I had before. 

"Ok, but Google Docs is such a big and complicated project! If a company as big as Google can't figure it out, why would you be able to!". I think the root of the problem is the fact that Google is using such a complicated project. They use docx files which are only a bunch of gibberish, they use these abstract a file system to the point where it becomes worse than using the terminal for normal people. The fix to this would simply be to use 3 things. A markdown format, Git and a normal filesystem. The version history of Google Docs functions the same as Git on plaintext, a markdown format is plaintext and using a normal filesystem would make everything easier to manage. If we reduce this process down to just these things, the only points of failure become Git, the markdown parser and the thing that would send an email for a tag. 

Additionally to reducing the points of failure, this becomes simpler, lighter and more extensible. If I want to add another feature, I can just add another feature to the markdown format. 
