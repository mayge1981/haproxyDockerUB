1. Build Docker image 
   * docker build -t haproxydemoub:latest .
2. Modify haproxy.cfg to point to your docker host ip address    
3. Run Docker image
   * docker run --name haproxydemo -d -p 8080:80 --sysctl net.ipv4.ip_unprivileged_port_start=0 haproxydemoub:latest
