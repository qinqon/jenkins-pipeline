node {
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
    stage 'Run FT'
    echo "BEGIN run_ft"
    sleep 50
    echo "END run_ft"
}
