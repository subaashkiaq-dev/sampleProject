Prometheus.yml
rule_files:
scrape_configs:
  - job_name: "prometheus"
    static_configs:
      - targets: ["localhost:9090"]
        labels:
          app: "prometheus"
  - job_name: "node"
    static_configs:
      - targets: ["localhost:9100"]
        labels:
          app: "node"

--------------------------------------------------------------------------------------------------
Step 1: Created the ec2 Instance 
Step 2: Installed and configure the Prometheus, Node Exporter and Grafana
Step 3: Created a PromQL Query to see the Metrics of CPU
step 4: Create a dashboard to see the CPU usage 
Step 5: Create a Alert Rule to alert if the CPU usage goes more then 40%.
