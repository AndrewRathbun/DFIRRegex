# DFIRRegex
A repo to centralize some of the regular expressions I've found useful over the course of my DFIR career. I get sick of hunting down regular expressions all the time so this is my attempt to centralize it not only for myself, but also for others. 

Regex101 links were included for the purpose of showing the expected hits when using the regular expressions prior to using them for your own purposes.

# Useful Regular Expressions

| Title | Regex | Regex101 | Links/Source |
|---|---|---|---|
| Credit Card Numbers | `(^4[0-9]{12}(?:[0-9]{3})?$)\|(^(?:5[1-5][0-9]{2}\|222[1-9]\|22[3-9][0-9]\|2[3-6][0-9]{2}\|27[01][0-9]\|2720)[0-9]{12}$)\|(3[47][0-9]{13})\|(^3(?:0[0-5]\|[68][0-9])[0-9]{11}$)\|(^6(?:011\|5[0-9]{2})[0-9]{12}$)\|(^(?:2131\|1800\|35\d{3})\d{11}$)` | https://regex101.com/r/HeuLIg/2/ | https://ihateregex.io/expr/credit-card |
| Cut Folder Hierarchy | `.+(?=((\\|\/).+){2})` |  | https://regexlib.com/REDetails.aspx?regexp_id=12777 |
| Email Addresses | `[A-Za-z0-9._%+-]+(%20\|@)[A-Za-z0-9.-]+\.[A-Za-z]{2,4}` | https://regex101.com/r/qf1qdh/1 |  |
| IPv4 | `@"\b(?:(?:25[0-5]\|2[0-4][0-9]\|1[0-9][0-9]\|[1-9]?[0-9])\.){3}(?:25[0-5]\|2[0-4][0-9]\|1[0-9][0-9]\|[1-9]?[0-9])\b")` | https://regex101.com/r/Yj3q6l/1 | https://github.com/EricZimmerman/bstrings/blob/d95a1ad3972ba3857218561a0e1929762ebab65f/bstrings/Program.cs#L876 |
| IPv6 | `(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}\|([0-9a-fA-F]{1,4}:){1,7}:\|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}\|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}\|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}\|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}\|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}\|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})\|:((:[0-9a-fA-F]{1,4}){1,7}\|:)\|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}\|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9])\|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9]))` | https://regex101.com/r/elIUjL/1 | https://www.regextester.com/25 |
| Passwords | ` ^(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])(?=.*?[#?!@$ %^&*-]).{8,}$` | https://regex101.com/r/XQ4S1b/1 | https://ihateregex.io/expr/password/ |
| Phone Numbers | `^(\+\d{1,2}\s)?\(?\d{3}\)?[\s.-]?\d{3}[\s.-]?\d{4}$` | https://regex101.com/r/2OLXcu/1 | https://stackoverflow.com/a/16699507/15393449 |
| URLs | `(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()!@:%_\+.~#?&\/\/=]*)`| https://regex101.com/r/GeH6XU/1 | https://mathiasbynens.be/demo/url-regex https://url.spec.whatwg.org/#parsing https://ihateregex.io/expr/url |
| US Social Security Numbers | `^(?!0{3})(?!6{3})[0-8]\d{2}-(?!0{2})\d{2}-(?!0{4})\d{4}$` | https://regex101.com/r/XDAlwg/1 | https://ihateregex.io/expr/ssn/ |
| Username (Discord) | `^.{3,32}#[0-9]{4}$` | https://regex101.com/r/bXCZn7/1 | https://ihateregex.io/expr/discord-username/ |

# Regex Resources

* https://www.regular-expressions.info/ - probably the best resource for regex that I've found yet! Made by the author of [PowerGREP](https://www.powergrep.com/) and [EditPad Pro](https://www.editpadpro.com/)
* https://regex101.com/ - great for testing regular expressions
* https://www.mockaroo.com/ - great for generating fake data to test regex
