docker build . -t :<tag/version>

github - project features: - ghcr - image storage - github actions - workflow code - repository - code storage

kubernetes - ghcr
process Flow

developer -> writes Code -> stores in github

devops -> - github - workflow - Dockerfile

Flow - developer code -> push -> main (default branch) - on(push) -> main -> workflow -> dockerfile -> build -> store the image -> in ghcr - image -> kubernetes/deployment.yaml ( todo/manually )

Manual: - docker build ( automate ) ( github actions ) - docker image ( automate ) ( github actions ) - deployment.yaml image - kubectl apply -f .

sed -i '' "s|ghcr.io/kamesh-a/learning-github-actions:latest|kamesh:test|g" ./k8s-manifest/deployment.yaml
