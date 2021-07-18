# DFIRRegex
A repo to centralize some of the regular expressions I've found useful over the course of my DFIR career

# Useful Regular Expressions


https://www.tablesgenerator.com/markdown_tables#

| Title | Regex | Regex101 | Links |
|---|---|---|---|
| Credit Card Numbers | `(^4[0-9]{12}(?:[0-9]{3})?$)|(^(?:5[1-5][0-9]{2}|222[1-9]|22[3-9][0-9]|2[3-6][0-9]{2}|27[01][0-9]|2720)[0-9]{12}$)|(3[47][0-9]{13})|(^3(?:0[0-5]|[68][0-9])[0-9]{11}$)|(^6(?:011|5[0-9]{2})[0-9]{12}$)|(^(?:2131|1800|35\d{3})\d{11}$)` |  | https://ihateregex.io/expr/credit-card |
| Email Addresses | `[A-Za-z0-9._%+-]+(%20|@)[A-Za-z0-9.-]+\.[A-Za-z]{2,4}` |  |  |
|  |  |  |  |
| IPv4 | `@"\b(?:(?:25[0-5]|2[0-4][0-9]|1[0-9][0-9]|[1-9]?[0-9])\.){3}(?:25[0-5]|2[0-4][0-9]|1[0-9][0-9]|[1-9]?[0-9])\b")` | https://regex101.com/r/Yj3q6l/1 | https://github.com/EricZimmerman/bstrings/blob/d95a1ad3972ba3857218561a0e1929762ebab65f/bstrings/Program.cs#L876 |
| IPv6 | `@"(?<![:.\w])(?:[A-F0-9]{1,4}:){7}[A-F0-9]{1,4}(?![:.\w])")` |  | https://github.com/EricZimmerman/bstrings/blob/d95a1ad3972ba3857218561a0e1929762ebab65f/bstrings/Program.cs#L877 |
| Passwords | ` ^(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])(?=.*?[#?!@$ %^&*-]).{8,}$` |  | https://ihateregex.io/expr/password/ |
| Phone Numbers | ` ^[\+]?[(]?[0-9]{3}[)]?[-\s\.]?[0-9]{3}[-\s\.]?[0-9]{4,6}$` |  | https://ihateregex.io/expr/phone |
|  |  |  |  |
| US Social Security Numbers | `\d{3}-\d{2}-\d{4}` |  |  |
| Username (Discord) | `^.{3,32}#[0-9]{4}$` |  | https://ihateregex.io/expr/discord-username/ |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
| URLs | `(http(s?)\|ftp(s?)\|afp):\/\/(((www\.)?\w+\.(com\|org\|net)\|(\d{1,3}\.){3}\d{1,3}))`|  | https://mathiasbynens.be/demo/url-regex https://url.spec.whatwg.org/#parsing |




# To-Do
1. Add PowerGREP Library
2. fill out readme
3. Make Regex101 links for all the above to show how they work and don't work
4. add resources for regex
5. automate table of contents?
6. Add links for where expressiosn were found
