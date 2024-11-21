pipeline {
    agent any

        stages{
            stage('Build'){
                steps{
                    echo 'Building Please wait to srtong run Jenkins'
                }
            }
            stage('Test'){
                steps{
                    script{
                        def myvar = "Hello World!!"

                        if (myvar == "Hello World!!"){

                            echo"value Of myvariable:${myvar} Condition true"
                        }else if(myvar == "Goodbye, World"){

                        }else{
                            echo "Ok Condition false Condition is neither true nor false"
                        }    
                    }
                    echo 'Ok surprises To Runing test'
                
                }
            }

        }
}