This document outlines the steps to set up and test New Relic monitoring on an AWS-hosted WordPress application. It includes agent installation, dashboard configuration, and synthetic monitoring setup (Using New Relic Free tier).


## New Relic Overview
New Relic is a powerful Full-Stack observability platform that provides real-time insights into application performance, infrastructure health, digital experience monitoring and more.
This PoC focuses on deploying a WordPress site on AWS and integrating New Relic for monitoring. The goal is to track performance, analyse application behavior, and gain insights using New Relic’s observability tools.

### **Key Features Used in This PoC:**
- **APM (Application Performance Monitoring)**
- **Infrastructure Monitoring**
- **Synthetic Monitoring**
- **Dashboarding & Alerting**

## Steps Followed

1. **Installed and Configured New Relic PHP Agent**

   - On Application monitoring, selected PHP ![On a host (CLI)](../New-Relic-images/PHP-on-a-host-CLI.png).
   - ![Selected the package manager](../New-Relic-images/package-manager.png).
   - On the App server, added New Relic repository and installed the PHP agent.
   - Connected infrastructure and logs.
   - Restarted the Apache server to apply changes. 
   - ![Checked connection](../New-Relic-images/test-connection.png)

2. **Monitored Key Metrics in New Relic**

   - **Application Performance**: ![Tracked Resquest & response, connection uptime and error response codes](../New-Relic-images/App-performance.png).
   - **Infrastructure Monitoring**: Analysed CPU, memory, disk I/O and network usage of the EC2 instance![App server monitoring](../New-Relic-images/infra-monitor.png).
   - **Synthetic monitoring**: Since the WP site doesn't have any actual interactions, I used synthetic monitoring to ping checks that monitor uptime, page load speed and API availability from different regions ![synthetic](../New-Relic-images/synthetic.png).

2. **New Relic service map**
    ![service map](../Architecture-Diagrams/New-relic.pdf).

## **Conclusion**
This PoC successfully demonstrates how New Relic can be integrated into an AWS-hosted WordPress application to gain real-time insights into application performance, infrastructure health, logs, uptime, and various types of telemetry. By monitoring key metrics such as response times, server resource usage, and external service calls, New Relic provides actionable data to optimize both the application and infrastructure.