# WAH Public API 
###### V 1.0.0

------

### Get Server List

Return Game Server List 

* API: [BaseURL]
* Method: POST
* Arguments:  

    | Params        | Value           
    | ------------- |-------------
    | method      | server_list
    
* Response: Json List Server Name

Ex:
```json
[
    "COA_BETA",
    "COA_GAMMA"
]
```

------

### User Information
Return User Information associated with **SohaID** and **GameServer**

* API: [BaseURL]
* Method: POST
* Arguments:  

    | Params        | Value           
    | ------------- |-------------
	| method      | sh_user_info
   | shID            | SohaID
   | serverID     | GameServerID

* Response: User Information in JSon format

Ex:
```javascript
{
    "jid": "56ef6a4cc4cb50415ee0e38d",             // WAH ID
    "server": "COA_BETA",                          // GameServerID
    "_lastLogin": 1458709524663,                   // Last Login Time (Unix time)
    "gameData": {
        "Level": 8,                                // Profile Level
        "Avatar": 0,                               // Profile AvatarID
        "Frame": 0,                                // Profile AvatarFrameID
        "Name": "HuySOHA",                         // Profile Name
        "VIP": 1,
        "Guild": {
            "Name": "guildNo57",
            "Role": "junior"
        }
    }
}
```