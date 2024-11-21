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
                        def myvar = "Goodbye, World"

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
            stage('for Loop'){
                steps{
                    script{
                        
                        for (int i =0; 1 < 5; i++){
                            echo "Iteration ${i}"
                        }
                    }
                }
            }
            stage('for loop'){
                steps{
                    script{
                        def mylist=["apple", "orange","bluepery" , "Banana", "watermilon"]

                        for(String fruit : mylist){
                            echo "Fruit==> ${fruit}"
                        }
                    }
                }
            }

        }   
}