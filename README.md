echo "dbuser" | docker secret create pg_user -
echo "mypassword" | docker secret create pg_password -
echo "mydatabase" | docker secret create pg_database -


sudo docker run -it --rm --net postgres_default --link postgres_default:postgres postgres psql -h postgres -U postgres
