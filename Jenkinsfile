pipeline {
  agent any
  stages {
    stage('One') {
	  steps {
	    echo "Hi, this is abhijeet ghosh"
		echo "Start cloning the deployable app repo."
		def gitURL = 'https://github.com/abghosh82/deployable_app.git'
		def branchName = 'master'
		checkout([$class: 'GitSCM', branches: [[name: "${branchName}"]], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'LocalBranch', localBranch: "**"]], submoduleCfg: [], userRemoteConfigs: [[ url: "${gitURL}"]]])
	  }
	}
	stage('Two') {
	  steps {
	    echo "Learning jenkins pipeline"
		echo "Move the deployable app to correct location."
		sh "sudo cp -r deployable_app /deployment_area/."
	  }
	}
	stage('Three') {
	  steps {
	    echo "Deploy"
		sh "/deployment_area/deployable_app.sh"
	  }
	}
	stage('Four') {
	  steps {
	    echo "Perform Unit Test"
	  }
	}
	stage('Five') {
	  steps {
	    echo "Perform Integration Test"
	  }
	}
	stage('Six') {
	  steps {
	    echo "Performance Test!!"
	  }
	}
  }
}