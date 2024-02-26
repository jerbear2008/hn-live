# Hacker News Live Feed
This is a live feed for viewing all of the new items on Hacker News in almost-realtime. It is a single, modern HTML file.

![Screenshot of the live feed](https://github.com/jerbear2008/hn-live/assets/38813665/780c89ef-6e17-43e9-8d38-178307cc6bc4)

It works by establishing a websocket connection to the Hacker News Firebase database, to receive updates every time the HN server updates Firebase, which is about once every 30 seconds. This is very efficient, putting no load on HN's server and using minimal bandwidth.

To make the feed continuous despite the delay, it waits to display each item until exactly 30 seconds before displaying it. I think this is a fair tradeoff, it gives you a sense of how active HN is. For comparision, there are something like 6-7 *thousand* tweets every *second*.

- [Official HN Firebase API](https://github.com/HackerNews/API)
- [Hacker News discussion](https://news.ycombinator.com/item?id=39509910)
