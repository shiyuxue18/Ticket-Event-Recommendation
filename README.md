# Ticket-Event-Recommendation
This projects intends to search nearby events and recommend events for users based on their favorite items and browsing history.
## AWS link
http://52.206.25.89/Jupiter/index.html
## functions
### login
The user can log in through demo username and password:
username: 1111,
password: 2222
### search nearby items
Once you logged in, the browser will fetch your address and serach nearby events based on TicketMasterAPI. 
### favorite items
You could collect the events you like by tapping the like buuton and they will show in My Favorites.
### Recommendation
Only when we have favorite items could we recommend events for users. We recommend events mainly based on favorite items and organized by cateogories and distance.
## structures
### database schema
Table users:
| user_id | password | first_name | last_name |
| :---: | :---: | :---: | :---: |
| 1111 | 2222 | John | Smith|

Table items:
| item_id | name | rating | address | image_url | url | distance |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1718vfG65OjF0A9 | 387 Music Presents: | 0 | Los Angeles | image_url | url | 4.79|

Table category:
| item_id | category | 
| :---: | :---: |
| 1718vfG65OjF0A9 | music |

Table history:
| user_id | item_id | last_favor_time |
|| :---: | :---: | :---: |
| 1111 | 1718vfG65OjF0A9 | 2018-08-18 16:03:03 |
### API format
login: ./login

search item: ./search?user_id=1111&lat=37.38&lon=-122.08

item history: ./history?user_id=1111

recommendation: ./recommendation?user_id=1111

logout: ./logout
## demo
https://drive.google.com/file/d/1FXt1LjeqOR-csru2bbqAbbP25ZuYTL7x/view