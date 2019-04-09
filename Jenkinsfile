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
		sh "ls -l"
		sh "rm -rf /deployment_area/deployable_app"
		sh "mkdir /deployment_area/deployable_app"
		sh "cp -r . /deployment_area/deployable_app/."
	  }
	}
	stage('Three') {
	  steps {
	    echo "Deploy"
		sh "bash /deployment_area/deployable_app/deployable_app.sh"
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