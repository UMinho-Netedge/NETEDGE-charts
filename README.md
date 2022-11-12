# NetEdge-MEP
The NetEdge-MEP is a ETSI-MEC compliant MEP.
You should first have a Kubernetes cluster configured and helm v3 installed to run it.

If you use it, please refer to:


### Create chart
```bash
#In the current directory
helm package .
```
### Usage
```bash
NS=<namespace>
RELEASE=<release>
# Replace the following parameters to properly connect to OSM mongodb
# Can both be replaced in the values.yaml or via cli
#  mongodb_addr
#  mongodb_port
#  mongodb_database
#  mongodb_password
#  mongodb_username

# Without replace
helm install -n $NS --wait --timeout 15m $RELEASE <chart_name> --debug
# With replace
helm install -n $NS --wait --timeout 15m $RELEASE --mongodb_addr=<...> --mongodb_port=<...> --mongodb_database=<...> --mongodb_password=<...> --mongodb_username=<...> <chart_name> --debug
```
