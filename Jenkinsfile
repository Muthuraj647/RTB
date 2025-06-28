try{
    currentBuild.result = 'SUCCESS'

    node{
        stage('Checkout'){
            echo "Checkout done"
        }
        stage('Lint check'){
            echo "Lint check done"
        }
        stage('Test'){
            echo "Test"
        }
        stage('Build'){
            echo "Build"
        }
        stage('Static Analysis'){
            echo "Static Analysis"
        }
        stage('Code coverage'){
            echo "Code Coverage"
        }
        stage('Artifacts'){
            echo "Artifacts"
        }
        stage('Registry Push'){
            echo "Registry Push"
        }
        stage('Docker Scan'){
            echo "Docker Scan"
        }
    }
}
catch (e){
    currentBuild.result = 'FAILURE'
    throw e
}
finally
{
    echo "Done"
}