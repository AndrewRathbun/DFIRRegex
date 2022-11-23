# DFIRRegex
A repository to centralize some of the regular expressions I've found useful over the course of my DFIR career. I get sick of hunting down regular expressions all the time so this is my attempt to centralize it not only for myself, but also for others. 

Regex101 links were included for the purpose of showing the expected hits when using the regular expressions prior to using them for your own purposes.

# Useful Regular Expressions

| Title | Regex | Regex101 | Links/Source |
|---|---|---|---|
| Age (Under 18) | `^(0?[1-9]{1}\|[1]{1}[0-7]{1})(\s\|[-])?(y(\s?)o\|yr([sz]?)\|year([sz]?)((\s\|[-])?(old)?)\|y)((\s?\|[-])(old)?)$` | [Regex101](https://regex101.com/r/oL1Cgs/1) | Digital Forensics Discord Server user `jball77` |
| BASE64 | `^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}\=\|[A-Za-z0-9+/]{3}=)?$` | TBD | TBD |
| Credit Card Numbers | `(^4[0-9]{12}(?:[0-9]{3})?$)\|(^(?:5[1-5][0-9]{2}\|222[1-9]\|22[3-9][0-9]\|2[3-6][0-9]{2}\|27[01][0-9]\|2720)[0-9]{12}$)\|(3[47][0-9]{13})\|(^3(?:0[0-5]\|[68][0-9])[0-9]{11}$)\|(^6(?:011\|5[0-9]{2})[0-9]{12}$)\|(^(?:2131\|1800\|35\d{3})\d{11}$)` | [Regex101](https://regex101.com/r/HeuLIg/2/) | [IHateRegex](https://ihateregex.io/expr/credit-card) |
| Cut Folder Hierarchy | `.+(?=((\\|\/).+){2})` | [Regex101](https://regex101.com/r/pS5urG/1) | [RegexLib](https://regexlib.com/REDetails.aspx?regexp_id=12777) |
| Email Addresses | `(([a-zA-Z0-9_\-\.]+)@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)\|(([a-zA-Z0-9\-]+\.)+))([a-zA-Z]{2,4}\|[0-9]{1,3})(\]?)(\s*;\s*\|\s*$))*` | [Regex101](https://regex101.com/r/qf1qdh/2) | [StackOverflow](https://stackoverflow.com/questions/9809357/regex-for-validating-multiple-e-mail-addresses) |
| Grab Everything Before the First Comma | `^.[^,]*(?=(\,))` | [Regex101](https://regex101.com/r/e5N4qz/1) | N/A |
| Filenames (Including Extension) | `[^\\\/:*?"<>\|\r\n]+$` | [Regex101](https://regex101.com/r/qsXeQ3/1) | [Regular Expressions Cookbook](https://www.amazon.com/Regular-Expressions-Cookbook-Solutions-Programming/dp/1449319432) |
| Filenames (Short/Suspicious) | `^[\w,\s-]{1,3}\.[a-zA-Z0-9]{2,4}$` | [Regex101](https://regex101.com/r/MCNzMw/2) | [RegexTester](https://www.regextester.com/104048) |
| Hash - MD5 | `[a-fA-F0-9]{32}` | TBD | TBD |
| Hash - SHA1 | `[a-fA-F0-9]{40}` | TBD | TBD |
| Hash - SHA256 | `[a-fA-F0-9]{64}` | TBD | TBD |
| Hash - SHA512 | `[a-fA-F0-9]{128}` | TBD | TBD |
| Hex | `/^#?([a-f0-9]{6}\|[a-f0-9]{3})$/` | TBD | TBD |
| IPv4 | `\b(?:(?:25[0-5]\|2[0-4][0-9]\|1[0-9][0-9]\|[1-9]?[0-9])\.){3}(?:25[0-5]\|2[0-4][0-9]\|1[0-9][0-9]\|[1-9]?[0-9])\b` | [Regex101](https://regex101.com/r/Yj3q6l/1) | [bstrings](https://github.com/EricZimmerman/bstrings/blob/d95a1ad3972ba3857218561a0e1929762ebab65f/bstrings/Program.cs#L876) |
| IPv4 (External Only) | `\b(?!0\.)(?!10\.)(?!100\.6[4-9]\.)(?!100\.[7-9]\d\.)(?!100\.1[0-1]\d\.)(?!100\.12[0-7]\.)(?!127\.)(?!169\.254\.)(?!172\.1[6-9]\.)(?!172\.2[0-9]\.)(?!172\.3[0-1]\.)(?!192\.0\.0\.)(?!192\.0\.2\.)(?!192\.88\.99\.)(?!192\.168\.)(?!198\.1[8-9]\.)(?!198\.51\.100\.)(?!203.0\.113\.)(?!22[4-9]\.)(?!23[0-9]\.)(?!24[0-9]\.)(?!25[0-5]\.)(([0-9]\|[1-9][0-9]\|1[0-9]{2}\|2[0-4][0-9]\|25[0-5])\.([0-9]\|[1-9][0-9]\|1[0-9]{2}\|2[0-4][0-9]\|25[0-5])\.([0-9]\|[1-9][0-9]\|1[0-9]{2}\|2[0-4][0-9]\|25[0-5])\.([0-9]\|[1-9][0-9]\|1[0-9]{2}\|2[0-4][0-9]\|25[0-5]))\b` | [Regex101](https://regex101.com/r/Ct1khx/1) | [StackOverflow](https://stackoverflow.com/questions/33453057/regex-to-only-match-public-ipv4-address) |
| IPv6 | `(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}\|([0-9a-fA-F]{1,4}:){1,7}:\|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}\|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}\|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}\|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}\|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}\|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})\|:((:[0-9a-fA-F]{1,4}){1,7}\|:)\|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}\|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9])\|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]\|(2[0-4]\|1{0,1}[0-9]){0,1}[0-9]))` | [Regex101](https://regex101.com/r/elIUjL/1) | [RegexTester](https://www.regextester.com/25) |
| MAC Address | ` ^([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})$` | [Regex101](https://regex101.com/r/TotZcR/1) | [StackOverflow](https://stackoverflow.com/questions/4260467/what-is-a-regular-expression-for-a-mac-address) |
| Passwords | ` ^(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])(?=.*?[#?!@$ %^&*-]).{8,}$` | [Regex101](https://regex101.com/r/XQ4S1b/1) | [IHateRegex](https://ihateregex.io/expr/password/) |
| Phone Numbers | `^(\+\d{1,2}\s)?\(?\d{3}\)?[\s.-]?\d{3}[\s.-]?\d{4}$` | [Regex101](https://regex101.com/r/2OLXcu/1) | [StackOverflow](https://stackoverflow.com/a/16699507/15393449) |
| Qakbot C2 | `(http\|https).*\:[0-9]{2,5}\/t5` | TBD | [Twitter](https://twitter.com/Kostastsale/status/1594902025334321154?t=sGcife-eJnyRfqc8-5hHag&s=19) |
| Remove trailing backslash from every line in a document | `\\+$` | [Regex101](https://regex101.com/r/qayALM/1) | |
| URLs | `(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()!@:%_\+.~#?&\/\/=]*)`| [Regex101](https://regex101.com/r/GeH6XU/1) | [mathiasbynens.be](https://mathiasbynens.be/demo/url-regex) [URL Spec](https://url.spec.whatwg.org/#parsing) [IHateRegex](https://ihateregex.io/expr/url) |
| Valid URLs (Excluding FP from above) | `\b((ht\|f)tp(s)?:\/\/\|www\.)+[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9]{2,}((\/)?([-a-zA-Z0-9@:%_\+.~#?&\/=]*)?)\b` | [Regex101](https://regex101.com/r/cQYupX/3/) | `jball77` |
| US Social Security Numbers | `^(?!0{3})(?!6{3})[0-8]\d{2}-(?!0{2})\d{2}-(?!0{4})\d{4}$` | [Regex101](https://regex101.com/r/XDAlwg/1) | [IHateRegex](https://ihateregex.io/expr/ssn/) |
| Username (Discord) | `^.{3,32}#[0-9]{4}$` | [Regex101](https://regex101.com/r/bXCZn7/1) | [IHateRegex](https://ihateregex.io/expr/discord-username/) |

# Regex Resources

* https://www.regular-expressions.info/ - probably the best resource for regex that I've found yet! Made by the author of [PowerGREP](https://www.powergrep.com/) and [EditPad Pro](https://www.editpadpro.com/)
* https://regex101.com/ - great for testing regular expressions
* https://regexr.com/ - serves as a regex IDE
* https://www.mockaroo.com/ - great for generating fake data to test regex
