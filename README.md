# space-shooter
An implementation of Couchbase Lite inside of Unity3D

# Requirements
- Unity 5.0.1 Personal Edition or higher
- .NET 2.0 API compatibility settings (This should be set already but sometimes it doesn't save.  Double check at Edit->Project Settings->Player Settings->Other Settings->API Compatibility Level)

#Note
This will not build for web player.  Web Player puts large amounts of restrictions on the available API, some of which Couchbase Lite makes use of.

#Instructions

To fully understand the power of this demo, you must do the following things:

1. Start up Couchbase Sync Gateway<br>
    `./sg.sh start`

2. Upload a Unity Asset Bundle to the gateway<br>
    ```
    cd scripts
    ./initialize_data.sh
    ```
3. Start playing the game
4. Dynamically change the ship model without interrupting gameplay.  The script is on a three second timer so that you have a chance to get back to the game before the change happens.<br>
    `./set_ship.py "alternateship"`

5. (optional) Change back to the default ship<br>
    `./set_ship.py "" #the empty string is required`
