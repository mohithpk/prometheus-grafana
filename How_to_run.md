#How to run the prometheus docker image

#Please note the prometheus.yml too be present in the location before running below command
docker run --restart unless-stopped -d -p 9090:9090 -v /home/ec2-user/prometheus:/etc/prometheus prom/prometheus

#How to run the nodeexporter docker image
docker run --restart unless-stopped -d -p 9100:9100 quay.io/prometheus/node-exporter:v1.2.2

#use this ansiblw command to run the above command
ansible all -i hosts -m shell -a "your command" --key-file /home/ec2-user/.ssh/id_rsa --become

#How to run the Grafana docker image
docker run --restart unless-stopped -d --name=grafana -p 3000:3000 grafana/grafana
https://grafana.com/grafana/dashboards/1860-node-exporter-full/ 1860
