Note: commented out the lines pertaining to the firewall...

Also removed these lines from devcontainer.json
´´´
"postStartCommand": "sudo /usr/local/bin/init-firewall.sh",
"waitFor": "postStartCommand"
´´´

Install firewall after wanted aditional setups
´´´
# Get a shell in your running container
docker exec -it your_container_name bash
# Inside the container, run the script using sudo
sudo /usr/local/bin/init-firewall.sh
´´´
