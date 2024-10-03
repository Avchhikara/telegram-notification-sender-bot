# telegram-notification-sender-bot
A bot to send notifications on telegram

## How it works?

It'll expose an API endpoint to send message to anyone who is registered with the telegram bot: [NotificationByAvnishBot](https://t.me/NotificationByAvnishBot)

Basically, following steps need to be followed: 

1. Start chat with [NotificationByAvnishBot](https://t.me/NotificationByAvnishBot)
1. Follow the instructions as prompted by the bot. 
1. Afterwards, you're now registered. Then to send notifications to yourselves. *To understand, how to send the notification, see the sections below*


#### Sending notifications

1. Follow the [registration steps](TK) to obtain your auth token. 
1. Then send a POST request to `/api/notifications/text` with the body containing: *notificationMessage*, *authToken*, *userId*. 
   * eg: 
       ```
       /api/notifications/text
       {
            "notificationMessage": "Hello, check this out: <link>",
            "userId": "useremail@email.com",
            "authToken": "randomStringTokenfajdkfjadfk"
       }
       ```
