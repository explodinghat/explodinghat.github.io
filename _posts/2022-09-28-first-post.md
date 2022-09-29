## It's alive!

This is the first blog post, the beginning of something, the end of something else (nothing).

As part of this blog I will be exploring use of various Cloud technologies, providing guidance and documentation about new features, and generally broadcasting my opinion on what I think works well and what could use some improvement.

I will be covering topics from the following areas: Azure, GCP, Terraform, Azure DevOps, DevTest labs, Automation, Docker, Kubernetes, Linux, Ansible - and maybe throw in a couple of other areas of interest too - like cooking or films. 

Everything will be geared towards getting things 'going' on a shoestring budget, with easily-repeatable and automated processes wherever possible. Any complex, resource-intensive configuration will be set up in a budget-conscious way with steps included for destruction - the idea being that it should be near impossible to spend over $10 following a guide here correctly. 

### The first tutorial

It would be nuts to set up a cloud tutorial/ how-to blog without adding a simple tutorial into the first post! So, let's start by setting up a new Azure PAYG account and setting up a DevTest Lab which we can use in the future to spin up short-term VMs, or a persistant VM that automatically shuts down at a specific time of day. The great thing about DevTest Labs is that the 'wrapper' it provides in Azure is completely free - so you can follow this guide to the letter without spending a penny (though you will need a credit card to sign up for Azure!)

#### Sign up for Azure Account

- Navigate to https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go/
- Click 'free account'
- Click 'start free'
- If you have an existing Microsoft/ Windows live/ Outlook account that has _never_ previously been used for Azure, you can sign straight in. Otherwise, click the link next to 'No account? Create one!'
- Click 'get a new email address' and follow the wizard through to create a new address to use for your azure subscription
- Log in to your new Azure account

#### Create the DevTest lab

- In the Azure search bar, search 'DevTest' and select 'DevTest Labs'
![DevTest Labs](https://blogblobmedia.blob.core.windows.net/blogblob/Screenshot 2022-09-28 at 16.50.40.png)
- Click on '+ Create'
![DevTest Labs creation screen](https://blogblobmedia.blob.core.windows.net/blogblob/Screenshot 2022-09-28 at 16.56.26.png)
- Make sure your Pay-as-You-Go subscription is selected
- Click 'Create new' under 'Resource Group' and create a new resource group for the lab
- Enter your chosen lab name and select your preferred location
- Select 'no' for 'Public Environments'
- Click the 'Auto-shutdown' tab
![DevTest Labs shutdown policies]
- Turn 'enabled' to 'on' and select a preferred shutdown time. You can also send an alert to a webhook or email address before the VM is switched off to avoid losing unsaved work.
- Click the 'Review and create' tab and then click 'create'

That's it! Your lab is now spinning up. My next post will explore some of the settings you can/ should change to a newly created lab, and I will also explore how to fire up and interact with VMs in future posts. Feel free to explore these topics yourself, but for now you've ticked off two major milestones - creating an Azure account and creating a DevTest lab - and you won't have spent a penny.

## About the blog

It's my intention (here on day 1, when everything seems rosy and bright and the whole world of Cloud is an open book to me) that I want to use the inbuilt features of GitHub as much as possible to host this blog, and I want anyone (who is so inclined) to be able to track my progress from Day 1 to whatever day it is you're eventually reading this. As such I will endevour to keep as much of this as open source as possible, including page revisions, code examples and projects, and not try to hide where I've subsequently edited a blog post or piece of code, or if I've just been plain wrong and had to eat my words! 

There will be plenty of stuff I need to figure out - such as how to store upcoming blog posts into a 'drafts' folder so that they don't show up when I push the repo with edits to existing posts (like this one, which I wanted to edit some 4 hours after originally published and will now be showing up alongside a draft piece I'm writing about the Azure Cloud Shell), how to change the layout and theme of the site, and also how to do basically anything interesting in the Cloud that people would want to read about! It could be a long journey.