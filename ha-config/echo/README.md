# Echo Service with High Availability and Clustering

This tutorial shows how to configure high availability using clustering and load balancing with Gateway.

### Getting Started

To run this you must have Docker installed and have added a host file entry for `kaazing.example.com`, as described [here](../../README.md)

The [docker-compose.yml](docker-compose.yml) describes two containers it will run, each an instance of the Gateway.

### Run

1. Start the containers
  ```bash
  docker-compose up -d
  ```
  
2. Connect to the Gateway in a Web browser via [http://kaazing.example.com:8000/](http://kaazing.example.com:8000/).  
3. Change the connect URL of the demo to `ws://kaazing.example.com:8000/` and connect.

4. When you send a message it should be echo back to you.

### Next Steps
  
[See Deployment Scenarios](../../README.md#deployment-scenarios)