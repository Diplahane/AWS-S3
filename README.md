# Static Website Hosting Using AWS S3

![Screenshot_20230620_130010](https://github.com/Diplahane/AWS-S3/assets/129828021/88b6db5b-3911-4183-aee6-f55f2ed373b8)

# Step 2: 

-Sign in to the AWS Management Console and navigate to the S3 service by searching for "S3" in the AWS Management Console search bar.

![Screenshot_20230620_130443](https://github.com/Diplahane/AWS-S3/assets/129828021/a58dc3ab-edea-4c17-b3bd-d5116c6aa22b)


 # Step 3:  

-Click on the "Create bucket" button to start the bucket creation process. 

![Screenshot_20230620_130513](https://github.com/Diplahane/AWS-S3/assets/129828021/adc3dad7-290e-4745-af99-b082a3aa34b3)



# Step 4:

-Provide a unique name for your bucket. This name will be part of the website URL, so it should be globally unique.

-Choose the region where you want your bucket to be located.  

![Screenshot_20230620_130739](https://github.com/Diplahane/AWS-S3/assets/129828021/f210a7dd-f1cd-435b-b01b-a51fb30005f6)

-Leave all other settings as their default values and click on the "Create" button to create the bucket.

![Screenshot_20230620_130751](https://github.com/Diplahane/AWS-S3/assets/129828021/fc34b2b2-40f7-4b07-a596-32187aaecb53)


# Step 5: 
![Screenshot_20230620_130823](https://github.com/Diplahane/AWS-S3/assets/129828021/56b5f56c-3284-413b-b7bd-9dead0e41f6e)

-Navigate to bucket "Properties"

![Screenshot_20230620_130850](https://github.com/Diplahane/AWS-S3/assets/129828021/e020a67e-7655-44a5-9cbc-57a5990d9693)

-Under "Static website hosting," click on the "Edit" button. 

![Screenshot_20230620_131006](https://github.com/Diplahane/AWS-S3/assets/129828021/2416c6e7-1789-4564-9833-0cadea66ec04)

-Select the option "Enable". 

-In the "Index document" field, enter the name of your main HTML file (e.g., "index.html"). 

-Optionally, you can provide a custom error document for handling 404 errors. 

-Click on the "Save changes" button.

![Screenshot_20230620_131223](https://github.com/Diplahane/AWS-S3/assets/129828021/7d999374-5f6f-4f48-8c99-deeec1bdba43)


# Step 6: 

Upload Website Files 

Open Notepad or any text editor and create a new file.

Write the desired content that you want to display on the website.

![Screenshot_20230620_131416](https://github.com/Diplahane/AWS-S3/assets/129828021/b4abbe98-07d1-42ca-8fc9-5349b32cb737)


Go to the "File" menu and click on "Save As".

Enter a file name for your webpage, ensuring that you include the ".html" extension, such as "index.html".

Click on the "Save" button to save the file.

![Screenshot_20230620_131531](https://github.com/Diplahane/AWS-S3/assets/129828021/62adeaed-3ee6-48bd-82db-0bd2c703a63c)



-Navigate to bucket "Object"

-Go to the "Upload" button or and click on it

![Screenshot_20230620_131602](https://github.com/Diplahane/AWS-S3/assets/129828021/fea165c0-2f8b-4672-a6f2-0d864e7bfbe2)



-Go to the "Add files" select the "index.html" file and then click on the "Upload" button

![Screenshot_20230620_131624](https://github.com/Diplahane/AWS-S3/assets/129828021/5663c46d-1831-44fe-b458-6788d7fb438b)


![Screenshot_20230620_131707](https://github.com/Diplahane/AWS-S3/assets/129828021/0b73f7e8-ee89-45b6-adf5-c55aee99115e)

![Screenshot_20230620_131727](https://github.com/Diplahane/AWS-S3/assets/129828021/4b9b8d4c-376e-463b-8828-5091c8664ee1)

-Once the upload is complete, you will see a confirmation message indicating that the file has been successfully uploaded.

![Screenshot_20230620_131739](https://github.com/Diplahane/AWS-S3/assets/129828021/201a7b7d-dac2-4fb9-bb9c-dda3e4137229)




# Step 6

-Enable Public Access 

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Block public access (bucket settings)" and click on "Edit."

![Screenshot_20230620_131813](https://github.com/Diplahane/AWS-S3/assets/129828021/79e43ee8-29a8-4efa-8e07-4b445a2e2171)



-Uncheck the box labeled "Block all public access" to allow public access to the bucket.

![Screenshot_20230620_131849](https://github.com/Diplahane/AWS-S3/assets/129828021/c7725df5-5b6f-41c7-bcb0-06abd5ba414a)



-In the designated field, type "confirm" to confirm your changes.

-this will will effectively enable public access for the bucket

![Screenshot_20230620_131924](https://github.com/Diplahane/AWS-S3/assets/129828021/86ae9715-dd6a-477b-9424-619cfb7acab1)

# Step 7

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Bucket policy" and click on "Edit."

![16ss](https://github.com/harshartz/AWS-EC2/assets/130890384/33343d96-3066-4c82-9d35-fb52d164761e)


-Click on "Policy Generator" it will open in a new window.

![17ss](https://github.com/harshartz/AWS-EC2/assets/130890384/8c2a1ca0-9f7f-4ba9-8117-8c06d156d97f)


-Select the type of policy as "S3" and set the effect to "Allow."

-In the "Principal" field, enter "*" to allow all the resourses.

-In the "Action" field, select "GetObject" to grant read access to the objects in the bucket.

-Paste the ARN (Amazon Resource Name) from the earlier tab into the "ARN" field.

-Click on "Add Statement" to include the generated policy.

![18ss](https://github.com/harshartz/AWS-EC2/assets/130890384/b20da9cb-c5dd-4c7e-aa93-9e7ff4df02a8)


-Copy the generated policy and paste it into the policy editor tab.

![19ss](https://github.com/harshartz/AWS-EC2/assets/130890384/232a17ab-2752-46e9-b0ec-1c3a18363b82)


-Add "/*" at the end of the resource to allow access to all files under the bucket.

-Click on "Save Changes" to apply the bucket policy.

![20ss](https://github.com/harshartz/AWS-EC2/assets/130890384/9d8b06bb-1838-4a38-8af7-4c2ef3adff7e)


-Navigate to the bucket's website endpoint and copy the provided link.

![21ss](https://github.com/harshartz/AWS-EC2/assets/130890384/2ac47666-0f5a-40a7-8ecd-f90e8783fb15)


-Open the link in a browser to verify if the website is functioning correctly.

-You should now see your static website live and accessible through the provided URL.

![22ss](https://github.com/harshartz/AWS-EC2/assets/130890384/4ae35226-5047-4bad-aed1-cdde36f6e7f1)



# That's it! You have successfully hosted a static website using AWS S3.
