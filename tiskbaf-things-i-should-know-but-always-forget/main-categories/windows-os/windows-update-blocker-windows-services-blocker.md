# Windows Update Blocker (Windows Services Blocker)

Windows 10 offers less UI control over the updating behavior of the operating system than previous versions of Windows , There is no option to turn off Windows Updates using the Control Panel or Settings app in Windows 10, it checks for updates automatically and install any updates they find, whether you like it or not. This new feature is actually pretty convenient for most users. If you want control over the update process you can disable the Windows Update service . This requires that you open the Services manager, locate the service and change its startup parameter and status. You would then have to enable the service again whenever you want the operating system to check for updates (It does not look so easy).\


Windows Update Blocker is a freeware that helps you to completely disable or enable Automatic Updates on your Windows system , with just a click of the button . This utility is portable, which means that you are no longer required to go through the installation process and no leftovers will remain on the HDD after its removal. if you place the program file to an external data device, you make it possible to take Windows Update Blocker everywhere with you and use it on any computer you come in contact with, who has things configured just right, and doesn’t want to take the chance that an update might mess up their system. This utility is for that person.

### **How it works**

After downloading, extract Windows Update Blocker to your desired location, then run it.The “Service Status Icon” will show the Windows Update service status , if you want to block Automatic Windows Updates Choose “Disable Service” And click “Apply Now” button. The Protect Service Settings checkbox can prevent Uncontrolled change **(Recommended)**.

### How to block any other service and protect the settings

The new version Windows Update Blocker allows users to add any other service into Wub.ini file to block it:

1. First, please edit Wub.ini file and add your desired service name under the “dosvc=2,4” line. For example, if you want to block “Windows Update Medic Service”, please open services and find it, then click on it and copy the “Service Name”.
2. Write in or paste the service name under the “dosvc=2,4” line within the Wub.ini file.
3. Open Windows Update Blocker and use “Apply now” button to apply your changes.

#### How to delete your recently added service in Windows Update Blocker

1. Open Windows Update Blocker and choose enable service option then use Apply now button.
2. Delete your desired service line from the Wub.ini file.
3. Now you can choose “Disable Service” and check the Protect service settings options.

#### Service List Options

Under Menu button there is a “Service List Options”. If you click it, a Service List Options popup window will be open. With this GUI you can easily control services which added to Wub.ini \[Service List] section. You can add a maximum of 25 services to the Wub.ini file. Wuausrv service showing only for informational purposes therefore you can not edit it.NOTE: If Windows Update Blocker can’t manage some of the services, they can be damaged, please use windows Update Troubleshooter fromM[icrosoft](https://support.microsoft.com/en-us/help/4027322/windows-update-troubleshooter)and If you don’t follow these steps and just delete any service from the “Wub.ini” file the service status will remain protected.
