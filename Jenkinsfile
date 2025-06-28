//RTB Railway Ticket Booking Application
//Author - Muthuraj647

def getBuildType(){
    echo "${env.JOB_NAME}"
    return "release"
}

def checkOutFunc(String url,String branch){

    // ! -d .git --> checks if .git file exists, git clean -fdx will remove all files, directories (d), not tracked files (x) forcefully (f)
    
    sh '[ ! -d .git ] || git clean -fdx'
    try{
        if(branch != null){
            checkout([$class: 'GitSCM', branches: [[name: "*/${branch}"]],
            userRemoteConfigs: [[url:url]]
            
            ])
        }
    }
    catch(e){
        printStackTrace(e)
        echo 'Failed to checkout'
    }
}


def checkoutGitProject(configs){
    buildType = getBuildType()

    if(buildType == 'release'){
        checkOutFunc(configs.gitURL, configs.gitBranch)
    }
}


def projectConfigs = [

    gitBranch   : "${params.PROJECT_BRANCH}",
    gitURL      : "https://github.com/Muthuraj647/RTB",
    projectDir  : "RTB",

]

try{
    currentBuild.result = 'SUCCESS'

    node{
        stage('Checkout'){

            checkoutGitProject(projectConfigs)
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