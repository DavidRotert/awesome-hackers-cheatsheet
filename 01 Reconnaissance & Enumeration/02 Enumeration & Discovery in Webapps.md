#enumeration #fuzzing #discovery 
# 01 Webcontent enumeration
- [[ffuf#Webcontent enumeration]]
# 02 VHost enumeration
- [[ffuf#VHost enumeration]]
# 03 Enumerate usernames/emails via password reset/login forms
**WARNING!** This is a very aggressive method and will either not work because of blocking mechanisms, give detection alerts or at least raise suspicion! Only use this if you are sure that the form does not have any rate limit etc.

- [[ffuf#Enumerate usernames/emails via password reset form]]
# Download exposed .git directory
#git #code
Sometimes, `.git` directories are exposed because innocent developers just deploy their webapps by pulling from a Git repo and don't protect the folder via deny rules in the webserver. This leads to exposure of source code.
- To download the contents, there is a tool called `git-dumper`. The bazingly fast Rust version: [[Git-dumper]]
# Tipps for Discovery
- On Hack The Box, VHost and content discovery is key!
- Search for Names, usernames and email addresses on the site! Note everything, even if it seems irrelevant at first. Sometimes these usernames or emails can come handy and are used later on for #pivoting and #lateral-movement in combination with weak and/or reused credentials
- If you have the source code, search it for usernames and email addresses (just search for the company domain for example `@example.com`) in configs and comments