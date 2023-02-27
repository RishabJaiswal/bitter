### Getting Slack access token

1. Open https://api.slack.com/apps
2. Click `Create New App` button
3. Select `From an app manifest`
4. Select Workspace where you are going to use it
5. Select `JSON format` on manifest editor page and paste this code:
```json
{
    "_metadata": {
        "major_version": 1,
        "minor_version": 1
    },
    "display_information": {
        "name": "Raycast - Set Slack Status"
    },
    "oauth_config": {
        "scopes": {
            "user": [
                "emoji:read",
                "users.profile:write",
                "users.profile:read",
                "users:write"
            ]
        }
    },
    "settings": {
        "org_deploy_enabled": false,
        "socket_mode_enabled": false,
        "token_rotation_enabled": false
    }
}
```

6. Press `Next` and then `Create`
7. In the sidebar select `OAuth & Permissions`
8. Press `Install to Workspace` button in `OAuth Tokens for Your Workspace` section
9. Once installed, you'll be able to copy your access token in `OAuth Tokens for Your Workspace` section. 
   It starts with `xoxp-`.