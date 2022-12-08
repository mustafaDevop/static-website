AWS-static-website
•	Deploy Static website to AWS with S3 and  Cloud Front.


Requirement: Basic understanding of AWS

Overview: Create an s3 bucket. Upload your files to the s3 bucket. Cloud front will reach out to Amazon s3 bucket to get the website content to serve the user.

Architecture

                                         
    LET’S GO!!
STEP 1.  LOGIN INTO YOUR AWS CONSOLE
•	Choose a region (I was using us-west2(Oregon)
•	NOTICE: REGION is very IMPORTANT  cause what is created at London will not able available in Oregon
![region_dashboard](https://user-images.githubusercontent.com/94189602/206501973-22ed57ee-0116-4aaf-809b-2ab1b596b7ac.PNG)

                           

•	Go your search bar at the right-hand corner

                                 
•	Click on s3 bucket and you will in the default page  


                            
•	Create bucket (in put bucket name and the region you want the bucket to be and be very careful of the name of the bucket NO symbols and just name.
•	If it going to be public bucket find a unique name, but right here we will be creating a public bucket


                             

•	Enable public access and acknowledge 
                                                    
•	Create button

                                                                      
•	Successfully created

                               

•	Now go back the dashboard and  click on your bucket name mine is “project102”

                                

•	Upload a file or folder your choice and its two ways of uploading either by drag and drop or by browsing. Now click upload 
                                  

•	Add file
                     

•	File added

                      

•	Upload file

                                        
•	Now go into your project and navigate to permission

       

•	Bucket policy. If bucket policy is empty then type in the code.

                          

•	Save it
•	Now go to properties and enable static website hosting, and don’t forget, index document and be the name of the html file you uploaded the main page. Mine is learn.html
           

•	Copy the endpoint of the bucket somewhere cause we using in the cloud front.


                         

•	Go to the search button and search for cloud front


                       

•	And click on distribution when you in the dashboard of cloud front. Paste the endpoint you copied in the origin domain and remove the http://. Cause if you don’t remove it wont work.
                


•	Default cache behavior. For the viewer enable turn it to redirect HTTP to HTTPS
                     

•	Create distribution


                                                    

•	Now copy your domain name it’s going to show your html file 

                    

•	Copy the domain name paste it in your browser you going to get a result
•	And copy the end point, paste it in the browser you going to get your result 
•	Copy and paste the URL in the file 
•	Here is the result
My endpoint http://project102.s3-website-us-west-2.amazonaws.com
Here is my domain d2t093g3jc6k5n.cloudfront.net
Access it while it last.
  
    
  
