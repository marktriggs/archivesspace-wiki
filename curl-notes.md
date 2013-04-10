
get JSON object

```sh

export session=`curl -s -F password=password http://localhost:8089/users/admin/login | jq -r .session`

curl  -s -H "X-ArchivesSpace-Session: $session" http://localhost:8089/repositories/5/resources/7 | jq . > object.json

```