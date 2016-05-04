node("remote") {
    git 'https://github.com/qinqon/jenkins-pipeline.git'
    parallel restore_and_deploy: {
        parallel restore : {
            stage 'vCBA restore'
            echo "BEGIN restore CBA"    
            sleep 10
            echo "END restore CBA"
        }, epb_delivery: {
            stage 'Create vSAPC delivery'
            echo "BEGIN epb delivery"
            sleep 5
            echo "END epb delivery"
        },
        failFast: true
        stage 'Apply vSAPC delivery'
        echo "BEGIN epb apply"
        sleep 30    
        echo "END epb apply"

    }, compile_ft: {
        stage 'Compile FT'
        echo "BEGIN compile_ft"
        sleep 10
        echo "END compile_ft"
    },
    failFast: true
    node("remote") {
       stage 'Run OAM FT'
       echo "BEGIN run_oam_ft"
       sleep 10
       echo "END run_oam_ft"
    }
    node("remote") {
       stage 'Run MOBILE1 FT'
       echo "BEGIN run_mobile1_ft"
       sleep 10
       echo "END run_mobile1_ft"
    }
    node("remote") {
       stage 'Run MOBILE2 FT'
       echo "BEGIN run_mobile2_ft"
       sleep 10
       echo "END run_mobile2_ft"
    }
}
