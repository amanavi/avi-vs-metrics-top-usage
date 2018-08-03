# avi-vs-metrics-top-usage
AVI-SDK based Script to get a list of VIPs using highest Bandwidth or no of Connections

 Created on August 3, 2018
 @author: aman@avinetworks.com

 AVI-SDK based Script to get a list of VIPs using highest Bandwidth or no of Connections

 Requires AVI-SDK:  sudo pip install avisdk==17.2.11b1
 Real Time Metrics in AVI needs to be enabled for the VIPs

 Usage:-
  python vs_metrics_top.py -c <controller-ip> -u <user-name> -p <password> -t <tenant> -a <api-version> -l <limits> -s <step> -pm <parameter>
  python vs_metrics_top.py -c '10.140.196.5' -u 'admin' -p 'Admin@123' -t 'admin' -a '17.2.11' -l '10' -s '300' -pm 'bw'

 step denotes the duration granularity of the metrics aggregation.
 step=300 means the average, sum, max etc are computed using metrics in 5min duration window.
 The metrics API would return one value every 5min as denoted by step.
 Avi solution supports step=300,3600,86400 values.

 Here are some examples
 1. Get metrics for last 6hrs: limit=72 & step=300
 2. Get metrics for last 1day: limit=288 & step=300
 3. Get latest single metric: limit=1 & step=300
