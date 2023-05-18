# Google Dork CheatSheet

## Search filters
| Filter          | Description                                        | Example                              |
| :-------------- |:---------------------------------------------------| :------------------------------------|
| allintext      | search for occurrences of all the given keywords. | `allintext:"keyword"` |
| intext      | search for the occurrences of keywords all at once. | `intext:"keyword"` |
| inurl      | search for a URL matching one of the given keywords. | `inurl:"keyword"` |
| allinurl      | search for a URL matching all of the keywords in the query. | `allinurl:"keyword"` |
| intitle      | search for occurrences of keywords in title. | `intitle:"keyword"` |
| allintitle      | search for occurrences of all keywords. | `allintitle:"keyword"` |
| site      | Specifically search that particular site and lists all the results for that site. | `site:"www.google.com"` |
| filetype      | search for a particular filetype mentioned in the query. | `filetype:"pdf"` |
| link      | search for external links in pages. | `link:"keyword"` |
| numrange      | Used to locate specific numbers in your search. | `numrange:321-325` |
| before/after      | Used to search within a particular date range. | `filetype:pdf & (before:2000-01-01 after:2001-01-01)` |
| allinanchor (and also inanchor)      | This shows sites which have the keyterms in links pointing to them, in order of the most links. | `inanchor:rat` |
| allinpostauthor (and also inpostauthor)      | Exclusive to blog search, this one picks out blog posts that are written by specific individuals. | `allinpostauthor:"keyword"` |
| related      | List web pages that are “similar” to a specified web page. | `related:www.google.com` |
| cache      | Shows the version of the web page that Google has in its cache. | `cache:www.google.com` |

## Examples

```
intext:"index of /"
Nina Simone intitle:”index.of” “parent directory” “size” “last modified” “description” I Put A Spell On You (mp4|mp3|avi|flac|aac|ape|ogg) -inurl:(jsp|php|html|aspx|htm|cf|shtml|lyrics-realm|mp3-collection) -site:.info
Bill Gates intitle:”index.of” “parent directory” “size” “last modified” “description” Microsoft (pdf|txt|epub|doc|docx) -inurl:(jsp|php|html|aspx|htm|cf|shtml|ebooks|ebook) -site:.info
parent directory DVDRip -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory MP3 -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory Name of Singer or album -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
filetype:config inurl:web.config inurl:ftp
“Windows XP Professional” 94FBR
ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) (intext:confidential salary | intext:"budget approved") inurl:confidential
ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) (intext:confidential salary | intext:”budget approved”) inurl:confidential


-site:www.digikala.com site:*.digikala.com   #search subdomains
```

# Operators

## Search Term

This operators search for the exact phrase within speech marks only.  This is ideal when the phrase you are using to search is ambiguous and  could be easily confused with something else, or when you’re not quite  getting relevant enough results back. For example:

```
"Tinned Sandwiches"
```

## OR
This self explanatory operator search for a given search term OR an equivalent term.

```
site:facebook.com | site:twitter.com
```

## AND

```
site:facebook.com & site:twitter.com
```

## Operators combinaison

```
(site:facebook.com | site:twitter.com) & intext:"login"
(site:facebook.com | site:twitter.com) (intext:"login")
```

## Include results

This will include all facebook domains with all TLDs.

```
+site:facebook.*
```

## Exclude results

This will search all facebook TLDs but exclude .com

```
site:facebook.* -site:facebook.com
```

## Glob pattern (*)

Putting an asterisk in a search tells Google is good for finding half remembered song lyrics! or names of things you want.

```
site:*.com
```

chack out GHDB (Google Hacking Database) of Exploit-db: [https://www.exploit-db.com/google-hacking-database]
