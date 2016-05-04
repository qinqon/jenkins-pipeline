node("remote") {
    git 'https://github.com/qinqon/jenkins-pipeline.git'
    parallel restore_and_deploy: {
        parallel restore : {
            stage 'vCBA restore'
            sleep 10
        }, epb_delivery: {
            stage 'Create vSAPC delivery'
            sleep 5
        }
        stage 'Apply vSAPC delivery'
        sleep 30    

    }, compile_ft: {
        stage 'Compile FT'
        sleep 10
    }
    parallel run_oam: 
    {
       node("remote") {
          stage 'Run OAM FT'
          sleep 120
       }
    }, run_mobile1: {
       node("remote") {
          stage 'Run MOBILE1 FT'
          sleep 120
       }
    }, run_mobile2: {
       node("remote") {
          stage 'Run MOBILE2 FT'
          sleep 120
       }
    }
}
