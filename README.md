# Container Scanning
## Container Scanning with Trivy
Directly scan public docker hub images
```sh
trivy image node:20.18
```
You can scan images from other registries
```sh
trivy image cgr.dev/chainguard/node:latest
```
Also from Gitlab registry
```sh
trivy image registry.gitlab.com/Your-Org/application/payments:d283208c --username XXXXX --password XXXXX
```
You can also login to registry via docker and then scan the images.

Docker Login (put your Gitlab access token when prompted):
```sh
docker login   registry.gitlab.com/Your-Org  -u XXXXX
```
Scan Image:
```sh
trivy image registry.gitlab.com/Your-Org/application/payments:d283208c
```
Docker Logout:
```sh
docker logout   registry.gitlab.com/Your-Org
```
