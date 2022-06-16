
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

Linking Fusion 360 to Apple Devices is a **three-Step Process**  

‼️It's very important to install and **run it in the presented order**‼️

1. Make sure you Have **iDrive installed** on the device running Fusion 360  
2. **iOS App** Installation
3. **Fusion 360** Add-In Installation

## 1.1 iDrive

### _Mac_ 
* Make sure both Devices are **connected to the Same Apple ID** - then everything should work fine. 
 
### _PC_
* If you **haven't installed iDrive** (it's something like Dropbox) go on with installing it start here:  
[Apple iDrive for Windows Info Page](https://support.apple.com/en-us/HT204283 "Title") or [Download iCloud for Windows from the Microsoft Store](https://www.microsoft.com/store/apps/9PKTQ5699M62 "Title")
* Make sure both Devices are **connected to the Same Apple ID** - then everything should work fine  

## 1.2 iOS App Installation 

1. Go to the Apple App Store and Download Fusion AR LINK TODO: **insert Applink**
2. Install and open it 
3. If you can see the welcome screen you're halfway done. 👏

## 1.3 Fusion 360 Add-In Installation

* 	Open Fusion 360 and **go to the Appstore** 

![Alt Image Text][locate_ADD-IN] 

* TODO: add detailed Install Steps from Screenshots in the Autodesk Store

### There will be a Picture of the app in the Autodesk Store

* **Open** your coolest **Model in Fusion **
* Navigate to ADD-IN and click the "Send to iDrive Button" ![Alt Image Text][Link_Icon]


![find_Fusion_App_Store][locate_ADD-IN] 

* TODO: add iOS Screenshot
### There will be a Picture of the app in the Autodesk Store

* Open the iOS App **Fusion-AR-LINK** the new File should appear automatically. 

## 2.0 <a name="Hints"></a>Hints / Known Issues
**2.1 Install Problems Mac**
>* Make sure your accounts both are linked to the same Apple ID. 
>* Reboot (Sometimes iDrive is having a hard time syncing)
  
**2.2 Install Problems Windows**
>* Make sure your accounts both are linked to the same Apple ID. 
>* No Known issues 

**2.3 Can't set iCloud Path**  
>* Make sure you have installed iCloud correctly and you've run the app at least once
>* A Fusion-AR-Link Folder with this README.md file should be in it.   
> If the Folder is empty restart the iOS App
>* Set exacty that folder when you're asked to do so, or set it in the Preferences ![Alt Image Text][Preferences_Icon] 

Found something else?  
📧 [bugsandfeatures@fakery.at]() 📧

##3.0 <a name="GenInfo"></a>General Product Information
**What it is:** 

>Fusion AR Link is a **"one click" Pipeline from Fusion360** (a well know 3D modelling software mostly used by hobbyists) to **the Quicklook Viewer known** from Apple devices. 

**How it worked until now:** 
>The known workflow was to export the file manually from Fusion to iCloud or Dropbox and reopen it in a sererate iOS Viewer. 

**Known Painpoints were:**
>* Manual Process (at least seven clicks and some taps)
>* Versioning was not handled well
>* Non-ASCII Characters led to bugs in the Viewer
>* resulting in a poor User Expirience

**Where we are now:**
>* One Click
>* Versioning and ASCII Conversion is handeld on the Fusion Add-In Side
>* File Exchange is performed via iCloud
>* iOS Observer catches filechanges on the iCloud and opens the model
>* User can easily share AR Models from the iOS Quicklook Interface

**Big Functionalities I'd like to add in upcoming Versions:**
>* Add custom Image Anchors (Define a Image Anchor in Fusion 360 -> Print it and the AR Model will be anchored to the printed Image)
>* Make a Pipeline the other way round. Scan an Object with your Device and import it as Mesh into your Fusion Design.  
>* share Files With different Groups (via public iCloud)
>* Maybe some glasses in Apple ecosystem might fall from the sky ?

**Small Changes I'd like to add in upcoming Versions:**
>* show Info Pop-up for Matiarials that are not soppuorted in usd

**What I havn't tested yet:**
>* iPad Pro with Wide Angle Camera - Would Love to see you Feedback 

**About Me:**
>* Working in VFX since 15 Years my Company Fakery offers Photorealistic Compositions for Advertising.
>* I got into coding not so long ago, so please be nice 🙏

####------------ The following part will be deleted in the Final README ------------ 


## 4.0 <a name="iOSAppstore_Val"></a>Specific for iOS Appstore Validation 

**This Readme will be placed in the App by default and hosted on Github**
Luckily the heavy Lifting is Done on the Fusion 360 Side. 

However, some General Infos about the app you might find helpful:
The App Consists of two screens. The syncing Process and the tableviewController are derrivatives from [this Example in the Apple Developer Section](https://developer.apple.com/documentation/uikit/documents_data_and_pasteboard/synchronizing_documents_in_the_icloud_environment)
the selected Row is then opend as Quicklook item. Changes in the conneced "iCloud+Appidentifier/Documents" Folder are automatically reflected in the Tableview. While running the app new Items (coming from the Fusion 360 ADD-IN) are automatically loaded. Files can be deleted with a swipe on the cell.  

At startup the readme and a sample Scene with Instructions is loaded.

Below the TableView three Info messages appear depending on the actual filecount.

If no scenes were added via the Fusion 360 Addin a help message is displayed there. 

* The purchase/restore options and status can be reviewed 
* An encouragment to rate the app
* The posibillity to contact me

**in App Puchase**. 
* The free Part of the app has the possibility to display the 5 most recent Usergenenrated Files + Readme + Sample Scene. After purchasing "Unlimited Models" the user has the possibility display an unlimited Amount of Usergenerated Files.   
* On the autodesk Side the ADD-IN is free

Branding of the AppIcon and the AppName are subject of the Autodesk Validation Process and may be changed to comply with their regulations. 

**Known Issues**
* Quicklook previews are generated in the background, when a new Thubnail in Higher resulution is genereated the Thumbnail and the height of the tableview updates.  

**Safety**  
The only way of data imported and getting shown to the User comes from it's personal iCloud Container. So the User only sees content created on his or her own. Therefore no special warnings or user protection Methods were implemented. The Links placed in the app are pointing towards help or additional resources. 
 


## 5.0 <a name="AutodeskstoreVal"></a>Specific for Autodeskstore Validation

**This Readme will be placed in the App by default and hosted on Github**

**Error Handling:**  

[Sucess_Info]: pictures/Sucess_Info.png 
[Sucess_NoInternet]: pictures/Sucess_NoInternet.png 
[SetPath]: pictures/SetPath.png 
[FailureInfo]: pictures/FailureInfo.png 
[FolderAlreadySet]: pictures/FolderAlreadySet.png 

Locating the Fusion-AR-LINK folder is the most common error. In the first place the script tries to locate the standard user Path. 
If this doesn't work out the User is prompted to set the Path to iCloud manually
It can also be changed in the Preferences Pop-Up. 

If no valid Path is Found the User gets a Info Message with a step-by-step help and the possibility to drop a line.  
![FolderAlreadySet][FailureInfo]  
If the export was a sucess the prompts look like this:
![FolderAlreadySet][Sucess_Info]
This handles the case Fusion is Offline and ther may be a syncing issue
![FolderAlreadySet][Sucess_NoInternet]
If the Folder was already set correctly a prompt appears:
![FolderAlreadySet][FolderAlreadySet]

**Technical Questions:**
>* Is there a way to place the Button Icons as Vectors ? They Appear so pixelated..
>* What is best practice for Adding python Libraries to an Addin so they work with every architecture and python version update?
>* I'd like to add [PyiCloud](https://github.com/picklepete/pyicloud) that can upload Files directly to iCloud. The Benefit would be that users don't need to download and setup the iDrive of Windows computers. I'd use [keyring](https://github.com/jaraco/keyring) to manage the automatic login process and to store the key. Do you have any technical concerns about this idea?
>* Do you have plans to extend the possibilities of the exporter? Supporting Animations and Complex Materials?  

**Branding Questions:**
>* How should I name your product inside the App Store Description to comply with your Brand?
>Fusion360 ,Fusion 360 , Fusion 360™ , Autodesk Store, Autodesk™ Store?
>* Would you call it an "Add-in" like the Button inside Fusion360 or an "App" (because of the Autodesk App Store)?  
>* Is the iOSApp-Branding (Name: Fusion AR Link) OK for you? Do you have any concerns ?
>* Do you have impressive models that I could set inside the sample scene, without copyright restrictions?
# FusionArLink
