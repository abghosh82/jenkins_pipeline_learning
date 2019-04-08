pipeline {
  agent any
  stages {
    stage('One') {
	  steps {
	    echo "Hi, this is abhijeet ghosh"
		echo "Start cloning the deployable app repo."
		git url: 'https://github.com/abghosh82/deployable_app.git'
	  }
	}
	stage('Two') {
	  steps {
	    echo "Learning jenkins pipeline"
		echo "Move the deployable app to correct location."
		sh "ls -l ../"
		sh "cp -r ../deployable_app /deployment_area/."
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