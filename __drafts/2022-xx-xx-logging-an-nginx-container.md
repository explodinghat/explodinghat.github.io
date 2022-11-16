# Logging in an nginx container

OK, some of the posts here will be a bit basic, as another hope I have for using this blog is just to note down 'little' things I find in my day-to-day and use them as reinforcement for learning. 

In testing DNS for my site - this site in fact - I set up port-forwarding to an nginx docker container hosting a simple splash page. My initial plan was to shut this back down once DNS for the site was sorted, but I'm actually going to keep this up, probably put a small micro-site up and pad out the monitoring, security and management of this container so that I can ensure it stays online, has increased hardening against external attacks, and I can view a log of illicit attempts to interact with the site. 

# The watch command

The watch command is pretty cool, this can give you a live view of access to your site/ page. The log is stored on the host by default, so assuming this is a linux machine you can run this command on the host:

`watch -n 1 cat /var/log/nginx/access.log`