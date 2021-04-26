# [Lift The Veil project](https://devpost.com/software/lift-the-veil-7-challenge#updates)
Presented For [Siemens Mobility](https://www.mobility.siemens.com/global/en.html) at [HackZurich](https://hackzurich.com) 2020, The Euorpe's most known Hackathon located at Zurich.

![](https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/221/507/datas/gallery.jpg) 

I made a team of five talented persons for this project and we came up with this solution. This repo does not contain all files.

# Inspiration
When driving in bad weather conditions, train drivers often cannot see signals and track-side equipment in front of their engine. They have to speed down in this situation just because they can't see outside like before. Now think about the passengers which can't see the beauty outside. boring!

# What it does
Using provided geotagged video and data of the train route, we will give the drivers insight when bad weather. There will be a Mobile app for their tablet. With that, they can see what's going outside, what's the nearest track sign, and how far they are from it and where is the train on the map. Very same thing for a passenger, who wants to see outside so they won't get bored seeing nothing outside, or maybe just a smart TV in the wagon for all!

# How we built it
As we needed to be as realtime as possible and other limitations like internet outages on the way, We had to cache data to the mobile client as well as doing some calculation there. Alongside the heavy-duty of the mobile app, we designed a back-end system in which mobile clients get files needed to cache. 

![](https://res.cloudinary.com/devpost/image/fetch/s--PS6GuyYq--/c_limit,f_auto,fl_lossy,q_auto:eco,w_900/https://raw.githubusercontent.com/MalekMFS/hackzurich2020/master/backend-architecture.png)

Our Flask app will be called to retrieve the new video and meta-data from the cloud storage (S3 in our case) and it will start compressing the video to the proper settings as well as cleaning invalid data on its meta-data and saving them on the server. On the other hand, Nginx will serve these files to the clients.


### [More info and Video](https://devpost.com/software/lift-the-veil-7-challenge#updates)
