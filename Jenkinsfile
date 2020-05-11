pipeline
{
	agent any
	stages{
		stage('Build Application'){
		steps{
		bat 'mvn clean install'
		}
		}
		
		stage('MUnit Testing Application'){
		steps{
		bat 'mvn test'
		}
		}
		
		stage('Deploy Application to CloudHub'){
		steps{
		bat 'mvn package deploy -DmuleDeploy'
		}
		}
		
		stage('Perform Regression Testing'){
		steps{
		bat 'C:\\Users\\NitishJain\\AppData\\Roaming\\npm\\newman run C:\\nik\\newman\\Test_Coll.postman_collection.json -r htmlextra --reporter-htmlextra-export C:\\nik\\newman'
		}
		}
}
}