<br>

<h1 align="center">SQLite3 Commands</h1>

<br>

<h3 align="center">Select Queries</h3>

<br>

Select Adlists

```sh
sqlite3 "/etc/pihole/gravity.db" "SELECT address FROM adlist"
```

Select Addresses by Domain Entries (number=0)

```sh
sqlite3 "/etc/pihole/gravity.db" "SELECT address FROM adlist WHERE adlist.number=0"
```

<br>

<h3 align="center">Delete Queries</h3>

<br>

Delete Empty (exact domains = 0) and (invalid_domains = 0)

```sh
sqlite3 "/etc/pihole/gravity.db" "DELETE FROM adlist WHERE adlist.number=0 AND invalid_domains=0;"
```

Delete by Status (Unavailabe Lists)

```sh
sqlite3 "/etc/pihole/gravity.db" "DELETE FROM adlist WHERE adlist.status=4;"
```

<br>

<h3 align="center">Select Domains</h3>

<br>

Select Blacklist Regex

```sh
sqlite3 "/etc/pihole/gravity.db" "SELECT domain FROM domainlist WHERE type=3"
```

