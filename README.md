
#Fusion AR Link Help and Info ![Alt Image Text][Link_Icon] ![Alt Image Text][Preferences_Icon] 

[Link_Icon]: pictures/32x32Link.png 

[Preferences_Icon]: pictures/32x32Pref.png 
[locate_ADD-IN]: pictures/locate_ADD-IN.png 
[find_Fusion_App_Store]: pictures/find_Fusion_App_Store.png

## Contents 
1. [Installation](#Installation)  
2. [Hints / Known Issues ](#Hints)  
3. [General Product Information](#GenInfo) 
4. [Information for iOS Appstore Validation](#iOSAppstore_Val)  
5. [Information for Autodesk Store Validation](#AutodeskstoreVal) 

## 1.0 <a name="Installation"></a> Installation

Linking Fusion 360® to Apple Devices is a **three-Step Process**  

‼️It's very important to install and **run it in the presented order**‼️

1. Make sure you have **iDrive installed** on the device running Fusion 360®  
2. **iOS App** Installation
3. **Fusion 360®** Add-In Installation

## 1.1 iDrive

### _Mac_ 
* Make sure both devices are **connected to the same Apple-ID** - then everything should work fine. 
 
### _PC_
* If you **haven't installed iDrive** (it's something like Dropbox) go on with installing it:  
[Apple-IDrive for Windows Info Page](https://support.apple.com/en-us/HT204283 "Title") or [Download iCloud for Windows from the Microsoft Store](https://www.microsoft.com/store/apps/9PKTQ5699M62 "Title")
* Make sure both devices are **connected to the same Apple-ID** - then everything should work fine  

## 1.2 iOS App Installation 

1. Go to the Apple AppStore and download Fusion AR Link TODO: **insert Applink**
2. Install and open it 
3. If you can see the welcome screen you're halfway done. 👏

## 1.3 Fusion 360 Add-In Installation

* 	Open Fusion 360 and **go to the Appstore** 

![Alt Image Text][locate_ADD-IN] 


* 	Install the Add-In
### There will be a Picture of the app in the Autodesk Store


*  You may need to enter your password and trust the developer

### There will be a Picture of trusting the Developer

* **Open** your coolest **Model in Fusion360®**
* Navigate to Add-In and click the "Send to iDrive Button" ![Alt Image Text][Link_Icon]


![find_Fusion_App_Store][locate_ADD-IN] 


* Open the iOS App **Fusion-AR-Link** the new file should appear automatically. 

## 2.0 <a name="Hints"></a>Hints / Known Issues
**2.1 Install Problems Mac**
>* Make sure your accounts both are linked to the same Apple-ID. 
>* Reboot (Sometimes iDrive is having a hard time syncing)
  
**2.2 Install Problems Windows**
>* Make sure your accounts both are linked to the same Apple-ID. 
>* No known issues 

**2.3 Can't set iCloud Path**  
>* Make sure you have installed iCloud correctly and you've run the app at least once. The iPhone app creates the "Fusion-Ar-Link" Folder. The Add-In searches for the link and saves the files inside. 
>* A Fusion-AR-Link Folder with this README.md file should be in it.   
> If the Folder is empty restart the iOS App
>* Set exactly that folder when you're asked to do so, or set it in the Preferences ![Alt Image Text][Preferences_Icon] 

Found something else? Drop us a line...
📧 [bugsandfeatures.fusion@gmail.com]() 📧

##3.0 <a name="GenInfo"></a>General Product Information
**What it is:** 

>Fusion AR Link is a **"one click" Pipeline from Fusion360®** (a well know 3D modeling software mostly used by hobbyists) to **the Quicklook Viewer known** from Apple devices. 

**How it worked until now:** 
>The known workflow was to export the file manually from Fusion360® to iCloud or Dropbox and reopen it in a separate iOS Viewer. 

**Known Pain-points were:**
>* Manual Process (at least seven clicks and some taps)
>* Versioning was not handled at all, files were overwritten
>* Non-ASCII Characters led to bugs in the Viewer
>* resulting in a poor User Experience

**Where we are now:**
>* One Click
>* Versioning and ASCII conversion is handled on the Fusion Add-In Side
>* File exchange is performed via iCloud
>* iOS observer catches new Files on the iCloud and opens the model
>* User can easily share AR Models from the well known iOS Quicklook Interface

**Big Functionalities I'd like to add in upcoming Versions:**
>* Add custom Image Anchors (Define an Image Anchor in Fusion 360® -> Print it and the AR Model will be anchored to the printed Image). Meaning you turn the image, you turn the object. You could then easily show the designed Object where it would sit in real life and compare proportions and scale.  
>* Make a pipeline the other way round. Scan an Object with your Device and import it as a Mesh into your Fusion Design.  
>* Share files with different Groups (via public iCloud)
>* The new RoomPlan API from Apple might also be interesting for Designers to quickly get a scale.  
>* Maybe some glasses might fall from the sky ?

**Small Changes I'd like to add in upcoming Versions:**
>* Show Info Pop-up for Materials that are not supported in usd
>* Make a promotion Video for the AppStore  
>* Add FAQ 

**What I haven't tested yet:**
>* iPad Pro with Wide Angle Camera - Would love to hear your feedback 

**About Me:**
>* Working in VFX since 15 Years my Company Fakery offers Photorealistic Compositing for Advertising.
>* Got into coding not so long ago, so please be nice 🙏
>


**Trademarks** 

Autodesk and Fusion 360 are registered trademarks or trademarks of Autodesk, Inc., and/or its subsidiaries and/or affiliates in the USA and/or other countries. There is no affiliation between the author of the App and Autodesk. The app is just providing a productivity Highway between two fascinating products.

####------------ The following part will be deleted in the User README ------------ 


## 4.0 <a name="iOSAppstore_Val"></a>Specific for iOS Appstore Validation 
**Introduction** 

This TestFlight is performed to find the last Glitches and get the Validation from Autodesk to list the corresponding Add-In in their Store.  


Luckily the heavy lifting is done on the Fusion 360® Add-In Side. 
However, here are some General Infos about the app you might find helpful:

**4.1 General Info**

The App Consists of two screens. 

**Main Screen:** Shows the Files  
**Preferences Screen:** inApp Purchases, QuickStart Tutorial,Detailed Help , About, Legal Infos, Contact Support

At startup a sample scene with Instructions is loaded.
Below the TableView an Info message appears depending on the actual file-count.

If one or no scenes were added via the Fusion 360 Add-In a help message is displayed there. 
After that an encouragement to rate the app is displayed


What happens under the hood:
The syncing Process and the tableviewController are derivatives from [this Example in the Apple Developer Section](https://developer.apple.com/documentation/uikit/documents_data_and_pasteboard/synchronizing_documents_in_the_icloud_environment)
the selected Row is then opened as Quicklook item. Changes in the connected "iCloud+App-identifier/Documents" Folder are automatically reflected in the Tableview. While running the app new Items (coming from the Fusion 360 ADD-IN) are automatically loaded. Files can be deleted with a swipe on the cell.  



**4.2 In-App Purchase**.  
>* The user can access(open & delete) the last three files that were uploaded. The remaining files are greyed-out and marked with an info that the purchase of the  "Supporter Pack" lets the user display all Files  
>* On the Autodesk Side the ADD-IN is free

**4.3 Known Issues**  
>* None

**4.4 Safety**  
The only way of data being imported and getting shown to the user comes from its personal iCloud Container. So the user only sees content created on his or her own. Therefore no special warnings or user protection methods were implemented. The Links placed in the app are pointing towards help or additional resources hosted on Github. 


**Some Elements are modified just for TestFlight:**  
>* Currently four sample Files are loaded at Startup to show a "populated" App. While these files are great for showcaseing functionality during testing, they should be replaced with more "technical" Fusion360® files to give the end product a less generic appearance. At the initial startup there should be one sample file so the "Quickstart-Tutorial" stands out in a more prominent way. The four files are now embedded in the App. They all get loaded at Startup, even after having been deleted. This is only for testing purposes
>* Some Screens in the "QuickStart Tutorial" and the "Detailed Documentation" are left blank because they can only be filled after the Autodesk Validation.  
>* Branding of the AppIcon and the AppName are subject of the Autodesk Validation Process and may be changed to comply with their regulations after TestFlight. 


## 5.0 <a name="AutodeskstoreVal"></a>Specific for Autodeskstore Validation

The script uses the builtin method to export a file from Fusion 360® to a given iDrive Folder. It handles sub-versioning and non ASCII-Character renaming. In the iPhone App the user gets a QuickStart Video Tutorial that will be extended with the downloading and the install process, once the plugin is listed. Since the user needs to download the app first no further "Video Tutorial" or "Screencast" is planned for now. Below you'll find detailed Error Messages that help the user in case of any Issues.   



**Error Handling:**  

[Sucess_Info]: pictures/Sucess_Info.png 
[Sucess_NoInternet]: pictures/Sucess_NoInternet.png 
[SetPath]: pictures/SetPath.png 
[FailureInfo]: pictures/FailureInfo.png 
[FolderAlreadySet]: pictures/FolderAlreadySet.png 

Locating the iCloud folder is the most common error. In the first place the script tries to locate the standard iCloud Path. 
If this doesn't work out the user is prompted to set the path to iCloud manually.
The path can also be changed in the Preferences Pop-Up. 

If no valid path is found the user gets an info message with a step-by-step help and the possibility to drop a line.  
![FolderAlreadySet][FailureInfo]  
If the export was successful the prompts look like this:
![FolderAlreadySet][Sucess_Info]
This handles the case Fusion is Offline and there may be a syncing issue
![FolderAlreadySet][Sucess_NoInternet]
If the folder was already set correctly a prompt appears:
![FolderAlreadySet][FolderAlreadySet]

**Technical Questions:**



>* Is there a way to place the Button Icons as a vectors ? They Appear so pixelated, the system ones so crisp. 
>* What is best practice for Adding python Libraries to an Add-In so they work with every architecture and python version update?
>* I'd like to implement USD Tools with USD Schemas from apple. A majority of USD bundle might already be implemented. Is there Any way to access it ? 
>* I'd like to add [PyiCloud](https://github.com/picklepete/pyicloud) that can upload Files directly to iCloud. The benefit would be that users don't need to download and setup the iDrive of Windows computers. I'd use [keyring](https://github.com/jaraco/keyring) to manage the automatic login process and to store the key. Do you have any technical concerns about this idea?
>* Do you have plans to extend the possibilities of the exporter? Supporting Animations or Complex Materials?  

**Branding Questions:**  

Dear Branding or Legal Team   

This app is currently in a closed Beta State. I don't want to do anything wrong and have absolutely no legal background. I just know about doing it wrong might be costly so obviously everything will be changed so it will comply with your brand regulations. 

As I'm building a two way connection between two Applications I have to write a lot of times the Application and Store Names. On the one hand I want users to easily find the Application thats why the Name is very similar. On the other hand I want to make very clear that this is not an Autodesk App but you need Fusion360 to use it. (This is also a requirement from the Apple App Store). I feel the app is adding Value to both Companies. If you could provide me some answers to the questions below this would help me a lot.

>* How should I name your product (inside the App Store Description & Manual) to comply with your Brand?
>Fusion360 ,Fusion 360® , Fusion 360™ , Autodesk Store, Autodesk™ Store?
>* Would you call it an "Add-In" like the Button inside Fusion360 or an "App" (because of the Autodesk App Store)?  
>* Is the iOSApp-Branding (Name: Fusion AR Link) OK for you? Do you have any concerns ?
>* Do you have impressive Fusion360® models that I could set inside a sample scene, without copyright restrictions?
>* Please see examples below that I'd use for marketing as well as the iOS app itself. At the moment the Disclaimer can be found here:   
> /1. Description iOS AppStore. 
> /2. Inside each Screenshot where Fusion360® is mentioned.   
> /3. In the GitHub hosting the files.   
> /4. The legal GitHub section can be accessed through a link in the app. (Follow the Gear Symbol in the right upper corner, tap "Legal Acknowledgements "     
>* To preserve your trademark and exclude liabilities I'd use the sentence:    
>**"You'll need to have a valid Fusion 360 subscription and install the Add-in to enjoy full functionality.  
Autodesk and Fusion 360 are registered trademarks or trademarks of Autodesk, Inc., and/or its subsidiaries and/or affiliates in the USA and/or other countries. There is no affiliation between the author of the App and Autodesk. The app is just providing a productivity highway between two fascinating products. There is obviously no resulting liability from Autodesk or the author that future versions of Fusion 360 will support the run of the mandatory Add-on. "**   
>* Do I need to add it inside the App Preview (as it is now) or is it enough if I place it inside the Description?   
>* Am I missing a Place ?

Thanks a lot for the time you spent on reviewing my case. I'd also love get back to you before the final iOS Version is published at the AppStore, to be on the safe side... 

Greetings from Austria  
Pascal