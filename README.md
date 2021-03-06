



# FACE ATTENDENCE WITH AWS REKOGNITION 
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)    [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![star this repo](http://githubbadges.com/star.svg?user=rizwansoaib&repo=face-attendence)](https://github.com/rizwansoaib/face-attendence)
[![fork this repo](http://githubbadges.com/fork.svg?user=rizwansoaib&repo=face-attendence)](http://github.com/rizwansoaib/face-attendence/fork)


BUILD IN DJANGO WITH MYSQL DATABASES 

## Video Click to play
 [![video](https://user-images.githubusercontent.com/29729380/58380408-4cccee00-7fce-11e9-8e21-5e940188162c.jpg)](https://www.youtube.com/watch?v=Y6P1_nWpaUs)



# USE



## INSTALLATION

## 1. Install awscli in your system and configure: 
   ### MAC LINUX OR UNIX
     rizwan@ubuntu$ sudo apt-get install awscli
     /* FIND YOUR ACCESS KEY AND SECRET KEY FROM AWS IN SECUIRTY CREDENTIALS */
     rizwan@ubuntu$ aws configure
     
     enter details of access key and secret key
     
                              or
                              
     rizwan@ubuntu$ export AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE 
     rizwan@ubuntu$ export AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY 
     rizwan@ubuntu$ export AWS_DEFAULT_REGION=us-west-2
     
   ### WINDOWS 
        C:\> setx AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE
        C:\> setx AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
        C:\> setx AWS_DEFAULT_REGION=us-west-2
        
  ## 2. Import knit.sql DB
   ### Mysql CommandLine
      mysql>create database db_name;
      mysql> use db_name;
      mysql> source knit.sql;
   ### Terminal
      mysql -u username -p password db_name < knit.sql
   ### Windows Command Prompt
     mysql -p -u [user] [database] < knit.sql
   ### PowerShell
      C:\> cmd.exe /c "mysql -u root -p db_name < knit.sql" 
 ## 3. Add Databases in Django Project
   #### Go to face-attendence/web/web/settings.py 
     Replace NAME,USER,PASSWORD with your credentials
     
     
      DATABASES = {
      'default': {
    'ENGINE': 'django.db.backends.mysql',
    'NAME': 'db_name',
    'HOST': '127.0.0.1',
    'PORT': '3306',
    'USER': 'username',
    'PASSWORD': 'password',
     }}
     
 ## 4. Add your S3 name and path
   #### Go to face-attendence/web/face/views.py in upload function 
     Replace s3,object key name, with your credentials
     
 ## 5. Activate virtual environment
   #### Go into web directory
    
     source env/bin/activate
     
 ## 5. Run server
    python3 manage.py runserver
     



 ### Take class images and Upload it on our website-
  ![class](https://user-images.githubusercontent.com/29729380/55557299-32317380-5707-11e9-87ed-53bbc0f0edad.jpg)
  ![faceclass](https://user-images.githubusercontent.com/29729380/55557397-6147e500-5707-11e9-8c7e-33b70fc4829d.jpg)

  
  #### We are taking this photo as example
![example](https://user-images.githubusercontent.com/29729380/55557345-470e0700-5707-11e9-9a77-1d524236eb54.jpg)



   
 ### we stored images of student in s3 you can do it locally on your server
  ![s3_images](https://user-images.githubusercontent.com/29729380/55560046-087b4b00-570d-11e9-9126-2f4a9550423e.gif)

 ### Both images analyzing and detect faces and crop them
 ![output](https://user-images.githubusercontent.com/29729380/55559239-69a21f00-570b-11e9-85c6-acaa2ddf2e4b.gif)


#### Cropping face
 ![cropping-student](https://user-images.githubusercontent.com/29729380/55559774-8db23000-570c-11e9-9aca-0ffe66515a72.gif)
   
![cropping-class](https://user-images.githubusercontent.com/29729380/55559581-23998b00-570c-11e9-8901-f99c15209b70.gif)

 ### Now Matches face

      
  ![matching](https://user-images.githubusercontent.com/29729380/55560318-9820f980-570d-11e9-8cfc-960ed3be6914.gif)

## WebApp 
### Home,Student Register,Teacher Login,Student Login
![web](https://user-images.githubusercontent.com/29729380/58379963-3754c580-7fc8-11e9-8d0e-6f6e766d34b4.gif)

### Manual Attendance with single click

![manual](https://user-images.githubusercontent.com/29729380/58379961-3754c580-7fc8-11e9-9df7-fbff552a659e.gif)

### Face Attendance Single Image required


![face](https://user-images.githubusercontent.com/29729380/58379960-36bc2f00-7fc8-11e9-9c41-dd3fce909e54.gif)


### Student Dashboard Attendance Report
![student](https://user-images.githubusercontent.com/29729380/58379962-3754c580-7fc8-11e9-8b08-4f644d852446.gif)



