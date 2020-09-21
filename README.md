# About db
Mini utility to store the list of the enumerated subdomains into an sqlite3 db. [one liner Style ]
# Prod
#### Install Requirements
`sudo pip3 install Flask flask_sqlalchemy loguru uuid`

> Add it as a bash command
```bash
cp db /usr/bin
chmod +x /usr/bin/db
```

# Usage

- Add list of subdomains to database

`cat subdomains.txt | db
`
or 

`echo example.com | db`

- Search for domain

`db <domain.com>`
