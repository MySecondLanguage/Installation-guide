# Install pgAdmin 4 with docker and connect local pc non container postgresql

run following command pgadmin 4
`sudo docker run -p 9000:80  -e "PGADMIN_DEFAULT_EMAIL=admin@example.com" -e "PGADMIN_DEFAULT_PASSWORD=admin"  -d dpage/pgadmin4`

hit this url: http://localhost:9000/ and login to via above credentials

### connect no-container postgresql with docker pgadmin 4

add `listen_address= '*'` in postgresql.conf file and change pg_hba.conf file with host all and host

Note: in pgadmin 4, you need to fill host section with `172.17.0.1` instead of `localhost`
