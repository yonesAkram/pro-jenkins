pipeline {
    agent any
        parameters{
            string(name: 'NAME', defaultValue: '', description: 'Enter your name')
            choice(name: 'EXPERIENCE', choices: ['less than 1', '+1', '+2', '+3','+4'], description: 'Select your experience')
        }//parameters        
        stages{
            stage('print OutPut'){
                steps{
                    script{
                        
                        def name = params.NAME
                        def experience = params.EXPERIENCE
                        echo "Your name is ${name} and you have ${experience} Years of Experience"
                    }//script
                }//steps('print output')

            }//stage('print OutPut')
            stage('Build'){
                steps{
                    echo 'Building Please wait to srtong run Jenkins'
                }//steps
            }//stage('Build'){
            stage('Test'){
                steps{
                    script{
                        def myvar = "Goodbye, World"

                        if (myvar == "Hello World!!"){

                            echo"value Of myvariable:${myvar} Condition true"
                        }else if(myvar == "Goodbye, World"){

                        }else{
                            echo "Ok Condition false Condition is neither true nor false"
                        }//else{    
                    }//script
                    echo 'Ok surprises To Runing test'                
                }// stage('Test'){ steps{
            }//stage('Test'){
            stage('for Loop'){
                steps{
                    script{
                        
                        for (int i = 1; i <= 5; i++){
                            echo "Iteration ${i}"
                        }//for
                    }//"for Loop"steps{ script}
                }//stage"for Loop" steps{
            }//stage('for Loop'){
            stage('for loop List'){
                steps{
                    script{
                        def mylist=["apple", "orange","bluepery" , "Banana", "watermilon"]

                        for(String fruit : mylist){
                            echo "Fruit==> ${fruit}"
                        }//for(String fruit : mylist){
                    }//stage('for loop list'){
                }//stage('for loop'){ steps Sound core R50i
            }//stage('for loop List'){


        }//Stages{}


           
    }//pipeline{}