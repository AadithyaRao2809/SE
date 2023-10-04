```# Use postgres/example user/password credentials

version: '3.1'  
services:
 
  db:
    image: postgres
    restart: always
    environment:
      POSTGRES_PASSWORD: 202002
      POSTGRES_USER: PES1UG21CS015
    ports:
      - "5432:5432"
      - 
  adminer:
    image: dpage/pgadmin4
    restart: always
    ports:
      - "5050:80"
    environment
      PGADMIN_DEFAULT_EMAIL: aayushsenapati2002@gmail.com
      PGADMIN_DEFAULT_PASSWORD: ******
```

1. docker -ps `container name`
2. get ip and put it in server
	- create server and add ip here and port 5432
	- same username and password as compose
3. to access: psql -U `USERNAME`
