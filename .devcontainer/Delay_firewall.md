Note: commented out the lines pertaining to the firewall...

´´´
# Get a shell in your running container
docker exec -it your_container_name bash
# Inside the container, run the script using sudo
sudo /usr/local/bin/init-firewall.sh
´´´
