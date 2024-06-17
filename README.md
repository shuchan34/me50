# YOUR Share Artists
#### Video Demo:  https://youtu.be/P91M4a5TdTg
#### Description:

I made an application that the users can share their favorite musical artists to other users and can also see the favorite artists of other people. I decided to make this application because I like music and I wanted to know some new musical artists from other people.  By sharing them, people can sympathize and be sympathized, and I thought it’s going to be a good opportunity for the users.

Now, I'm going to explain some functions of this webpage.

First, there is a 'register' page which users can make their new account. On this page, users must input username and password on the input field to make an account. Python is going to generate hash using the werkzeug.security library and keep them in the users table in the sql database.Then, it’s going to return ‘login’ page. When the users successfully logged in, it’ going to return ‘index’ page.

Then, users can select their favorite artists on the 'select favorite' page (first item on the menu bar). Users are going to input the name of the artist in the search field and click the search button. There will be a list of related artists returned  from the external sites so the users can select the ones they are looking for. When selected, the name of the artists is going to be saved in the mypage table in the sql databse.  Users can continue selecting up to three artists.

When the users made some mistakes while choosing their favorite artists, they can delete them anytime on the 'delete favorite' page (second item on the menu bar). Artists the users selected are shown on the page, so users can delete them by clicking the button. It is going to be deleted from the mypage table

Users can also see some favorite artists of other people on the 'other people's favorite' page (third item on the menu bar). On this page, users can see the artists that every other people have selected. The artists each users have selected is saved in the sql databese so those data are going to be pulled using execute function. 

Lastly, I’m going to explain what I used in this application. First of all, I used jinja2 templates from flask and got the output on the html from python. I got the data of the musical artists from the Japanese web page called Uta-Net (https://www.uta-net.com/) using bs4 library. I also used sql to keep my data organaized. I made two tables in my sql database. Users table is for keeping track of the usernames and their passwords. Mypage table is for housing the names of the musical artists. I linked the id of the users table and the user_id of the mypage table in order to know which artists each users chose.
