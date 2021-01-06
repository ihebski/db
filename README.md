# db
Mini utility to store the list of the enumerated subdomains into an sqlite3 db. [one liner Style ]

![Build Status](https://pbs.twimg.com/media/EiYn1w3XYAAAlN9?format=jpg&name=large)

Status: **Development**
## Features

* Remove duplicates
* Query database
* Clean results
* Pipe results to store data
* Export the saved records

## Chaining tools
You can pipe the subdomain tools results into db
argparse
> Example :

> subfinder + db
> ![Build Status](https://pbs.twimg.com/media/EiY1Sa1WsAIPSSp?format=jpg&name=large)


# Prod
#### Install Requirements
`sudo pip3 install Flask flask_sqlalchemy loguru uuid fire csv argparse`

> Add it as a bash command
```bash
cp db /usr/bin
chmod +x /usr/bin/db
```

# Usage

| Query                                | Command                    |
|--------------------------------------|----------------------------|
| Add list of subdomains               |  <code>cat subdomains.txt &#124; db </code> or <code>echo subdomains.txt &#124; db </code>  |
| Add  **ONE**  subdmain to database   | `db save tesla.com`        |
| Search for domain                    | `db search tesla.com`      |
| Get the new added subdomains         | `db new`                   |
| Export list of subdomains            | `db export tesla.com`  or if csv  `db export tesla.com csv`    |
| Remove all the database records      | `db wipe`                  |
| Remove records for a specific domain | `db removeall tesla.com`   |
| Remove **ONE** record                | `db remove tesla.com`      |
|  Get all the saved records             | `db  all`      |

> PS : 
> - Export function uses TXT format by default (if csv is not specified)
> - new arguments shows the latest saved records for that day only
