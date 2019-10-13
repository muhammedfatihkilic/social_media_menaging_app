# social_media_menaging_app
#facebook auto share message

import requests

acccess_token = input("Access tokeni giriniz: ")
message = input("mesajı giriniz: ")


API_ENDPOINT = "https://graph.facebook.com/102399201180143/feed"
# üstteki rakamı değiştir
data = {'message': message,
        'access_token': acccess_token
        }

# sending post request and saving response as response object
r = requests.post(url=API_ENDPOINT, data=data)

pastebin_url = r.text
print("The pastebin URL is:%s"%pastebin_url)


