(1) Build Docker image 
    docker build -t haproxydemoub:latest .
(2) Run Docker image
    docker run --name haproxydemo -d -p 8080:80 --sysctl net.ipv4.ip_unprivileged_port_start=0 haproxydemoub:latest