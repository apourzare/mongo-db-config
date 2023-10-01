# Configure MongoDB

## Step one
run command:
<br>
`docker exec -it <mongodb-docker-name> bash`
<br>

## Step two
run this command:
<br>
`mongosh -u <username> -p <password> --authenticationDatabase admin`
<br>
or
<br>
`mongosh -u <username> -p <password>`
<br>
or
<br>
`mongosh "mongodb://localhost:27017" --username <username> --authenticationDatabase admin`

## Step three

set permissions for user

### For create user
`use admin`
<br>
`db.createUser({ user: "<username>", pwd: "<password>", roles: [{ role: 'root', db: 'admin'}] })`

### For arley user 
`use admin`
<br>
`db.grantRolesToUser('<username>', [{ role: 'root', db: 'admin' }])`
