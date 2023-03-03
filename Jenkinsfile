pipeline {
	agent any
	stages {
		stage("SCM") {
			steps {
				git 'https://github.com/abhi0172/django-todo.git'
				}
			}
     		stage("Image") {
			steps {
				  sh 'sudo docker build -t todo:$BUILD_TAG .'
				  sh 'sudo docker tag todo:$BUILD_TAG abhishek0322/todo:$BUILD_TAG'
				  sh 'sudo docker run -dit -p 8000:8000  abhishek0322/todo:$BUILD_TAG'
				}
			}
				
