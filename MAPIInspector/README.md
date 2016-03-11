# MAPI Inspector for Fiddler
The Messaging Application Programming Interface (MAPI) Inspector for [Fiddler](http://www.telerik.com/fiddler) decodes the MAPI message payload of an HTTP POST request and response. The MAPI Inspector displays under the *Inspectors* tab in Fiddler.

This repository also includes Jscript that adds an *MS Protocol* column in the Fiddler web session panel. The *MS Protocol* column displays the protocols that are relevant to MAPI messages thereby allowing you to easily identify which HTTP requests and responses contain MAPI message payloads.

The MAPI inspector decodes the MAPI message payload according to [MS-OXCMAPIHTTP](https://msdn.microsoft.com/en-us/library/Dn530952(v=EXCHG.80).aspx).

## Installation 
Installation of the MAPI Inspector involves adding the DLL file and the MAPI script. Before installing these items, you must first install the latest [Fiddler](http://www.telerik.com/fiddler) tool and then run it. Note that Fiddler must be run at least once before installing the MAPI Inspector.

### MAPI Inspector DLL###
1. Copy the file [MAPIFiddlerInspector.dll](https://github.com/OfficeDev/MAPI-Inspector-for-Fiddler/blob/master/MAPIFiddlerInspector.dll) into the C:\Program Files\Fiddler2\Inspectors directory. Alternatively, you can clone this repository, build the MAPIFiddlerInspector.dll, and copy the built .dll to your C:\Program Files\Fiddler2\Inspectors directory.
2. Restart Fiddler. The MAPI Inspector will display under the *Inspectors* tab, as shown in the following screenshot, after restarting.

    ![alt tag](https://cloud.githubusercontent.com/assets/13864956/10044516/329c59c4-622e-11e5-9b68-8ef920d4ead8.jpg)

### MAPI Script ###

1. From the *Rules* menu, which is shown in the following screenshot, click *Customize Rules*.
    
    ![alt tag](https://cloud.githubusercontent.com/assets/13864956/10038377/a6e8d104-61f7-11e5-9a84-989fcf135f2c.png)

2. When the following message box displays, click the *Yes* button to install the FiddlerScript editor.

    ![alt tag](https://cloud.githubusercontent.com/assets/13864956/10044513/2d5a400c-622e-11e5-9b1c-3cb44c11eb15.jpg)

3. Restart Fiddler after the installation of the FiddlerScript editor completes. Fiddler displays a new tab, *FiddlerScript*, as shown in the following screenshot. Copy the code from the code from the [MAPI.js](https://github.com/OfficeDev/MAPI-Inspector-for-Fiddler/blob/master/MAPI.js) file and paste it into the definition for the **Handlers** class. Click the *Save Script* button to save the script.

    ![alt tag](https://cloud.githubusercontent.com/assets/13864956/10044440/9fc2b382-622d-11e5-8308-a642768bf28a.jpg)

4. Restart Fiddler. After restarting, the *MS protocol column* can be displayed in session view.

    ![alt tag](https://cloud.githubusercontent.com/assets/13864956/10045590/6689c232-6236-11e5-9751-0caf596b3bba.jpg)

