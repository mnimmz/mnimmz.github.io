---
layout: post
title:      "Vevo Trending Videos CLI Project"
date:       2018-04-24 22:56:15 +0000
permalink:  vevo_trending_videos_cli_project
---


I'm very happy to say that I finally finished my CLI Data Gem Project! Woo hoo! Boy, was it a challenging process but I managed to get through it, with my project actually working the way I wanted it to.

For my project, I wanted to create a YouTube Trending CLI project where the top four trending videos would be scraped from YouTube. To get started, I attended the **Project Prep: CLI Portfolio Project Office Hours** and the host answered a lot of my questions and gave me a good idea of where to start and what kind of functionality I might want to include in my project. Then, I watched Avi's **CLI Data Gem Walkthrough** video and it provided tremendous help as to how I should start to build my project and creating a gem from scratch using 'bundler' in the command line. Creating a Notes.md file, which Avi did in his own demonstration, to jot down ideas about my project and how I want things to work gave me a good foundation.

I followed along with the video walkthrough to build my project, but obviously there were a lot of things that I had to do different for my individual project, such as how I initialized a new object, how I structured my methods and I had to incorporate modules in order for my code to be more *DRY*. 

However, there were some setbacks. The major issue I had was the inability to scrape data from the Trending page on YouTube. I could pull data from the YouTube navigation, but when I used pry to see if I could scrape data from even first level divs, it would return an empty string. As a result, I had to utilize 1:1 Project Support. My technical coach and I had discovered that YouTube loads dynamic content using AJAX, which Nokogiri could not scrape from because the content was being loaded after Nokogiri would attempt to scrape any data. I was giving the option of either using a different a tool called Selenium to scrape data which would require me to spend time learning a new tool, or choosing a different website to scrape from. I obviously chose the latter to save time.

I wanted to still scrape trending music videos from a website, so I switched to pulling data from Vevo.com instead, which worked fine. However, Vevo did not provide much information about each trending video on the homepage, just the artist name and video title. A user would have to click on the video in order to learn more about the video such as its description and the amount of views its received. In order to make my project more interesting and interactive, I made it so it would only display the first 10 trending videos and if the user typed 'more,' the last 10 would be listed. If the user typed 'back,' the terminal would display all 20 trending videos from the site.

In order to still fulfill the requirement of providing list and detail views (i.e. "showing the user a list of available data and then being able to drill down into a specific item"), I still kept the functionality of the user typing the number next to one of the videos listed, and that video's information (video title and artist name) would solely be shown in the terminal. 

I'm pretty proud of myself that I was able to complete this project in a week and able to get it working correctly, without needing too much assitance. I'd say that I've definitely come a long way from when I first started Flatiron School. :)
