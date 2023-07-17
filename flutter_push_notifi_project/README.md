# flutter_push_notifi_project

A new Flutter project.

## Getting Started

After creating a new project and write down the necessey code, then you need to configure the firebase first. so that open a project in firebase console first, then create a android project with your already created flutter project id from app/build,gradle and add necessary dependencies code to configure the flutter project. Then you need to enable cloud messaging and cloud messaging API to get the server key.

now everything is ready. first run the flutter application. from here you will get the FCM Token for the device. then open Postman and create a POST request like below, where the request will be in json formate and paste FCM Token in regestration id option and also add a new option in request header like-  Key Name : Authorization, Value: key="cloud messaging API server key"

here the request body will be like below-

# Server PostMan Fire Payload
{
    "registration_ids": [
        "d1TBrY4CFUQ0i5eTC4Xy4l:APA91bEvNq94qttb2yZ-aUXSWesr9HWyFVKevUCoTE55JKrFLbi7H32qQ5ZcwPzkft580CId-sHSUE99zAbvXrvEITYwo0eLa1ofmIh3e91MqaKdQyRALJH181C-E4xK5QF2J4H3RDtk"
        
    ],
    "notification": {
        "title":"Test Push",
        "body":"Test Message Body",
        "android_channel_id":"push_notification_demo",
        "sound":true
    },
    "data": {
        "d_id":"1",
        "page":"detail",
        "title":"hi device push data",
        "user_login_need":"true",
        "user_id":"2"
    }
}


Now the send button and you will get a successfull message in postman and also get the push notification in your device.