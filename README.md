Developer Push code to a repository(e.g: Github)
A CI pipeline using Jenkins runs unit tests(Units tests, Integration Tests and Linting), Build stage (compile code and Create artifacts) and  then builds a  docker image for the application.
The image is tagged and pushed to a container registry (ECR), security scans on the image are performed in CI.
If all checks pass, the pipeline may trigger a deployment (CD phase).
Updates Kuberentes manifests with the new image and applied to the cluster using the helm upgrade
