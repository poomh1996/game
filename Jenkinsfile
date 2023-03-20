pipeline{
  
  agent{
     
	 label{
	 
	      label'built-in'
		  customWorkspace'/mnt/bliss'
		 }
}		 
		  
stages{

       stage('on-master'){
	   steps{
	     
		sh "rm -rf *"
	    sh "sudo yum install tree -y"
	    sh "sudo touch aishu"
		
		}
	}	
	  
 stage('on-slave-1'){
 
    agent{
        
         label{		
		 
		 label'slave-1'
	     customWorkspace'/mnt/frient'
            }
        }
      steps{
          
	      sh "rm -rf *"  
          sh "sudo yum install httpd -y"
          sh "sudo yum install tree -y"		
          sh "sudo touch aishu"
  
        } 
  }
  
  stage('on slave-2'){
  
    agent{
	
	   label{
	      
		  label'slave-2'
		  customWorkspace'/mnt/friend'
		  
		 }
		}
   

}


}
