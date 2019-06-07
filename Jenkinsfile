registry="index.docker.io"
credentials="/registry-config/registry.yaml"
image="harikarthi/makisu-sh"
tag="latest"

pipeline {
    agent {
        kubernetes {
            cloud "kubernetes"
            label "makisu"
        }
    }

    stages {
        stage ("build"){
            steps {
                container("makisu"){
                    sh """
                        /makisu-internal/makisu build \
                        --modifyfs=true \
                        --push=$registry \
                        --registry-config=$credentials \
                        -t=$image:$tag \
                        $WORKSPACE
                    """
                }
            }
        }
    }
}
