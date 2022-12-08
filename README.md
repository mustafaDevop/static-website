AWS-static-website
•	Deploy Static website to AWS with S3 and  Cloud Front.


Requirement: Basic understanding of AWS

Overview: Create an s3 bucket. Upload your files to the s3 bucket. Cloud front will reach out to Amazon s3 bucket to get the website content to serve the user.

Architecture

                                         
    LET’S GO!!
STEP 1.  LOGIN INTO YOUR AWS CONSOLE
•	Choose a region (I was using us-west2(Oregon).

•	NOTICE: REGION is very IMPORTANT  cause what is created at London will not able available in Oregon
![region_dashboard](https://user-images.githubusercontent.com/94189602/206501973-22ed57ee-0116-4aaf-809b-2ab1b596b7ac.PNG)

                           

•	Go to your search bar at the left-hand corner and type s3
![search_s3](https://user-images.githubusercontent.com/94189602/206503737-50e985a4-aa02-404e-add4-85ea97b5d465.PNG)

                                 
•	Click on s3 bucket and you will in the default page  

 ![s3_dashboard](https://user-images.githubusercontent.com/94189602/206503837-c158f4fe-a27f-4d24-bc8e-3d2b88f9f334.PNG)
     
•	Create bucket (input bucket name and the region you want the bucket to be and be very careful of the name of the bucket NO symbols and just name).

•	If it going to be public bucket find a unique name, but right here we will be creating a public bucket

![bucket_name](https://user-images.githubusercontent.com/94189602/206504222-73cf912b-ff63-43e4-80f9-dc1a4c093e24.PNG)

                             

•	Enable public access and acknowledge 

![public_access_s3](https://user-images.githubusercontent.com/94189602/206505105-79aba732-7c26-4f33-8ebe-bc6dc1034bc9.PNG)

                                                    
•	Create button

![create_button](https://user-images.githubusercontent.com/94189602/206505207-a53e7fa3-c9d8-4ed7-acf8-322d8465535d.PNG)

                                                                      
•	Successfully created

  ![successful_created](https://user-images.githubusercontent.com/94189602/206505259-ec892a6a-a393-470d-81a0-c719a5025422.PNG)
                          

•	Now go back the dashboard and  click on your bucket name mine is “project102”

   ![click_project_name](https://user-images.githubusercontent.com/94189602/206505484-a1f54688-1a0c-4e93-ae83-e21d9bc9bec5.PNG)
               

•	Upload a file or folder of your choice and its two ways of uploading either by drag and drop or by browsing. Now click upload 
          ![upload_file](https://user-images.githubusercontent.com/94189602/206505823-8216b194-2722-494d-94ba-42d4d51c052b.PNG)
                        

•	Add file
        ![add_file](https://user-images.githubusercontent.com/94189602/206505872-68243301-7914-4eaa-ae12-5b658aebb9c6.PNG)
             

•	File added

   ![file_added](https://user-images.githubusercontent.com/94189602/206505931-2c316d0f-f35f-4868-97be-e62564a6b0ad.PNG)
           

•	Upload file
![upload_file_html](https://user-images.githubusercontent.com/94189602/206505993-b3b472fb-41b0-410f-bdd9-8e3566ce9cce.PNG)

                                        
•	Now go into your bucket name just like you did and navigate to permission
![bucket+permission](https://user-images.githubusercontent.com/94189602/206506441-f4735acd-a96c-4232-a285-7af899a7899c.PNG)

       

•	Bucket policy. If bucket policy is empty then type in the code.

 ![fill_bucket_policy](https://user-images.githubusercontent.com/94189602/206506688-9fb0b76d-1376-450d-a136-daae721c1dfa.PNG)
    

•	Save it
![save_policy](https://user-images.githubusercontent.com/94189602/206506811-3f786bc6-0f04-4a5f-8448-54e6f77b71fc.PNG)

•	Now go to properties and enable static website hosting, and don’t forget, index document and be the name of the html file you uploaded the main page. Mine is learn.html
           ![step_static_web](https://user-images.githubusercontent.com/94189602/206507135-e7a4f280-7d91-4a9e-9754-f43c09ec86da.PNG)


•	Copy the endpoint of the bucket somewhere cause we using in the cloud front.

![enabled_hosting](https://user-images.githubusercontent.com/94189602/206507241-a644ec62-e0a6-4dc6-a61d-40fdd0b65bbf.PNG)

                         

•	Go to the search button and search for cloud front

![cloud_font](https://user-images.githubusercontent.com/94189602/206507316-432c2887-d3a4-408a-8588-09b5bbba9111.PNG)

                       

•	And click on distribution when you in the dashboard of cloud front. Paste the endpoint you copied in the origin domain and remove the http://. Cause if you don’t remove it wont work.
                
![set_cloudfon2](https://user-images.githubusercontent.com/94189602/206507566-e3d2614f-21a3-4273-95fa-2090e312991d.PNG)


•	Default cache behavior. For the viewer enable turn it to redirect HTTP to HTTPS
                     ![setup_cloudfront2](https://user-images.githubusercontent.com/94189602/206507865-21676535-5fbd-4d2c-a948-e68125a8ccde.PNG)


•	Create distribution

![create+distribution](https://user-images.githubusercontent.com/94189602/206507967-834b37e7-ffa6-4ad7-ac5d-466459883978.PNG)

                                                    

•	Now copy your domain name it’s going to show your html file 
![domain](https://user-images.githubusercontent.com/94189602/206508080-425c4a47-3e6a-4a62-8677-48536fe66493.PNG)

                    

•	Copy the domain name paste it in your browser you going to get a result

•	And copy the end point, paste it in the browser you going to get your result 

•	Copy and paste the URL in the file 

•	Here is the result

My endpoint http://project102.s3-website-us-west-2.amazonaws.com

Here is my domain d2t093g3jc6k5n.cloudfront.net

Access it while it last.
                 
  DOMAIN RESULT
    ![result1](https://user-images.githubusercontent.com/94189602/206508182-707e16ed-e62a-463e-b30e-07d4d280fac7.PNG)
      
   ENDPOINT RESULT 
       ![result2](https://user-images.githubusercontent.com/94189602/206508243-bae7b1d9-39a7-408b-9bab-3fa6f2dfd5ff.PNG)

