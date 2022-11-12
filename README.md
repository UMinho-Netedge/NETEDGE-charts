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
# Without replace
helm install netedge-mep <chart_name>
```
