# Autopsy-15.02.2015
Image Recovery

Name: Nirupama Bandara
Registration Number: MS13961718

1)Creating test partition on VMware and Kali Linux

2) Creating the dd image: http://www.howtogeek.com/howto/19446/make-a-drive-image-using-an-ubuntu-live-cd/

* Recovery process of the images using Autopsy

* Decrypting the hidden message of the recorded images by using QuickStego tool

Analyzing Disk Images Using “Autopsy” 


Autopsy is a digital forensics platform and graphical interface to The Sleuth Kit® and other digital forensics tools. It can be used by law enforcement, military, and corporate examiners to investigate what happened on a computer. 
Autopsy was designed to be an end-to-end platform with modules that come with it out of the box and others that are available from third-parties. Some of the modules provide: 

•	Timeline Analysis - Graphical event viewing interface. 

•	Hash Filtering - Flag known bad files and ignore known good. 

•	File System Forensic Analysis - Recover files from most common formats. 

•	Keyword Search - Indexed keyword search to find files that mention relevant terms. 

•	Web Artifacts - Extract history, bookmarks, and cookies from Firefox, Chrome, and IE. 

•	Multimedia - Extract EXIF from pictures and watch videos. 

#Step1: Log in to Kali, and then create a new folder to store data for this activity. We have crated folder called “jpgs”

#Step2: Then Go to the "Digital Forensics Tool Testing Images" Website and download hard disk image which contains corrupted JPEG image data 
	Go To http://dftt.sourceforge.net/ 
	Click on "8. JPEG Search Test #1" 

#Step3: Download the Image File “8-jpeg-search.zip”

#Step4: Once it has been downloaded, unzip the files in to the”jpgs” folder, we have crated earlier.

#Step5: Conduct an initial hard disk image integrity check 
Before using any tool to do an analysis on hard disk image, we need to have a way of showing the initial state of an unaltered image. md5sum does a mathematical calculation of the jpeg image. If Autopsy alters the image, this md5sum will change with our post Image Integrity Check. 

md5sum 8-jpeg-search.dd

#Step6: Then Start Up Autopsy 
Applications --> Kali Linux --> Forensics --> Forensic Suites --> Autopsy

#Step7: Once the AutoSpy has been loaded, copy the web URL that AutoSpy is running on to a web browser. 

#Step8: Once the AutoSpy web interface loaded, create a New Case.

#Step9: Fill the data necessary to create new AutoSpy case scenario. Then click on “New Case” button .Once New AutoSpy case has been created, we need to add New Host 

#Step10: To Add new Host, Just type Host Name and Click on “Add Host” button

#Step11: Once we have added New Host, we need to add hard disk image which contains forensics/bit level data of a computer.

#Step12: Get the file path of the image “8-jpeg-search.dd” file from a terminal and paste it in AutoSpy by clicking “Add Image File” button. 
ls $PWD/8-jpeg-search.dd

#Step13: Once the path of the Image file added, Click on “Next” button 
For Type, select the Partition Radio Button. 
For Import Method, Select the Symlink Radio Button. 

#step14: Finally click on “Add” button to add the image to AutoSpy database. 
For Data Integrity, select the "Ignore..." Radio Button 
Notice that Autopsy identified the File system type of the image as NTFS 

#Step15: Once the Image has been added to AutoSpy database, we can conduct an Image Integrity Check on added Image (MD5 CheckSum).

#Step16: Then we are going to Analyze Image with Autopsy. On the Case page, Click on “Analyze” button 
Then click on “Image Details” to View Image Details with Autopsy 
Viewing General File System Details with Autopsy 
Our Image

#Step17: Then click on “Image Details” to View Image Details with Autopsy

Step18: Viewing General File System Details with Autopsy 
Our Image File System Type is NTFS. If you made a backup of the original image, your Volume Serial Number should remain the same. This is important in a court of law, to demonstrate that the volume serial number of the image you analyzed is the same as the original copy.




