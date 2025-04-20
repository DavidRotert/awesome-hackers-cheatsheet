Fast **web fuzzer** written in Go.
#enumeration #fuzzing #discovery
## VHost enumeration
```
ffuf -u "http://127.0.0.1" -H "Host: FUZZ.example.org" -w "/usr/share/wordlists/seclists/Discovery/DNS/subdomains-top1million-5000.txt" -ic
```
Fine tune the output with **filters**.
## Webcontent enumeration
```
ffuf -u "http://127.0.0.1/FUZZ" -w "/usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt" -ic
```
Fine tune the output with **filters**.
## Enumerate usernames/emails via password reset form
**WARNING!** This is a very aggressive method and will either not work because of blocking mechanisms, give detection alerts or at least raise suspicion! Only use this if you are sure that the form does not have any rate limit etc.

```
ffuf -u "http://example.com/password-reset" -d "mail=FUZZ@example.com" -w "/usr/share/seclists/Usernames/Names/names.txt" -ic -fr "no valid mail"
```

## Filters
| Flag  | Description                                                                                                    |
| ----- | -------------------------------------------------------------------------------------------------------------- |
| `-fc` | Filter HTTP status codes from response. Comma separated list of codes and ranges                               |
| `-fl` | Filter by amount of lines in response. Comma separated list of line counts and ranges                          |
| `-fr` | Filter by regexp                                                                                               |
| `-ft` | Filter by number of milliseconds to the first response byte, either greater or less than. EG: `>100` or `<100` |
| `-fw` | Filter by amount of words in response. Comma separated list of word counts and ranges                          |
