# WAH Public API 
###### V 1.0.0

------

### Get Server List

Return GameServerID List 

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
Return User Information associated with **SohaID** and **GameServerID**

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
        "Diamond": 1603                            // Diamond
        "Name": "HuySOHA",                         // Profile Name
        "VIP": 1,
        "Guild": {
            "Name": "guildNo57",
            "Role": "junior"
        }
    }
}
```

------

### Reduce User Currency
Reduce in game currency associated with **SohaID** and **GameServerID**

* API: [BaseURL]
* Method: POST
* Arguments:  

    | Params        | Value           
    | ------------- |-------------
	| method      | sh_reduce_currency
   | shID            | SohaID
   | serverID     | GameServerID
   | amount     | Possitive number amount of currency
   | type | Currency Type ( Currently only support (Gold, Diamond) )

* Response: Error

```javascript
{
    "error": "Amount must greater than 0"       //Reason
}
```

* Response: Success

Ex:
```javascript
{
    "status": "ok"
}
```
