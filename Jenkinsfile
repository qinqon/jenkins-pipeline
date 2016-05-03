node {
	git 'https://github.com/qinqon/jenkins-pipeline.git'
	//parallel cba_restore: {
		echo "Restoring CBA"
        	sh "sleep 10"
    	//}, compile_ft: {
		echo "Compiling FT"
        	sh "sleep 5"
	//}, epb_delivery: {
		echo "Packaging vSAPC"
        	sh "sleep 5"
    	//},
	echo "Deploying vSAPC"
  	sh "sleep 5"
    	failFast: true
}
