# sms-sending-with-python
from twilio.rest import Client
account_sid = 'AC89f38addf3808447f7faecf15359e523'
auth_token = '7a3c5c6d100a36e8a2248223c357c280'

myPhone = '+254770103801'
TwilioNumber = '+13167764582'
client = Client(account_sid, auth_token)
client.messages.create(
    to=myPhone,
    from_=TwilioNumber,
    body='sent a message with code yay!!' + u'\u0001f680' )
