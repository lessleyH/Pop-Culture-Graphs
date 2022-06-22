# Pop-Culture-Graphs


## Kardashian- Jenner Graph
I created this for myself, because I saw a TikTok and got very confused when someone tried to explain to me how connected everyone was from dating.

I used python, networkx, and pyviz to create this graph. The data comes from TV interviews were Kardashian-Jenner family has confirmed their relationships and rumors, from their own TV show, and numerous news articles. A list of sources can be found bellow.

So there are family, friends, rumored relationships, and confirmed relationships on the graph. The family is the bold color, friends are the pinkish red color, confirmed relationships/flings/hookups/marriages/etc are green, and rumors are yellow.

![Kardashian Cinematic Universe Graph](https://user-images.githubusercontent.com/37605496/174937744-a3717226-a2f5-467b-bec6-0f63e37aef5e.png)


## Analysis

The network density is ```0.06095791001451379```, which is the ratio between actual edges versus all possible edges in the graph. The denser the network the closer to 1 the density is just to see how connected the graph is. 

The diameter of the graph is just 5, which is not suprising, because it is a very small graph. Hpwever that is the longest of all the shortest paths in the graph. So the diameter between the nodes that are farthest apart in the network is just ```5```. 

I also took the triadic closure which is a way to find triangles, like if a and b both know c then a and b should know of each other. For this graph the triadic closure is ```0.15604026845637584```. Notice how the density is lower than the closure so that means there are a lot of triangles that exist in this graph. But clearly with cheating and everything we know about this network I wonder what that could say about this network....

Clearly some of the most important parts of this graph is knowing the centrality basically who is the most important or if not has the most edges. This is the top 20 in just degrees: 
```
Top 20 nodes by degree:
('*Kim Kardashian', 23)
('*Kendall Jenner', 14)
('*Khloé Kardashian', 13)
('*Kylie Jenner', 11)
('*Kourtney Kardashian', 9)
('*Rob Kardashian', 6)
('Blac Chyna', 4)
('MGK', 4)
('Pete Davidson', 4)
('Tristan Thompson', 4)
('Jordyn Woods', 3)
('Justine Sky', 3)
('Travis scott', 3)
('Tyga', 3)
('Sofia Richie', 3)
('Justin Beiber', 3)
('Amber Rose', 3)
('Travis Barker', 3)
('Larsa Pippen', 3)
('James Harden', 3)
```
Which seems correct from everything we know about the Kardashian-Jenner family and the fact that this was a network of their relationships. Also, I took the betweeness centrality, which is nodes that connect clusters of the network. The higher the number the more likely these people broker information within this graph to different clusters. The top 20 nodes in that analysis:
```
Top 20 nodes by betweenness centrality:
('*Kim Kardashian', 0.5842023989082816)
('*Kendall Jenner', 0.2595022624434389)
('*Khloé Kardashian', 0.2463549522373052)
('*Kylie Jenner', 0.17991093873446806)
('*Kourtney Kardashian', 0.10783775048480934)
('Pete Davidson', 0.07236586942469293)
('MGK', 0.043094160741219564)
('Travis Barker', 0.038915822739352145)
('Blac Chyna', 0.0352204984557926)
('Larsa Pippen', 0.031737053795877324)
('Tristan Thompson', 0.0303921568627451)
('Tyga', 0.020293758529052647)
('Ciara', 0.01664152840623429)
('*Rob Kardashian', 0.014370107017165845)
('Kanye West', 0.011743158801982328)
('Kaia Gerber', 0.009064138475903184)
('Amber Rose', 0.007189542483660131)
('Jordyn Woods', 0.006561085972850679)
('James Harden', 0.0036450477626948216)
('Justine Sky', 0.003267973856209151)
```

I also tried to see if I could detect communities, but I don't think I choose the right partition for this network. Will definetely keep working on this. But currently it looks like this: 
```
Class 0: ['French Montana', '*Kendall Jenner', 'Anwar Hadid', 'Tyga', 'Devin Booker', 'Justine Sky', 'Younes Bendjima', '*Khloé Kardashian', 'Derrick Ward', 'Ben Simmons', 'Jordyn Woods', 'Justin Beiber', 'Tristan Thompson', '*Kylie Jenner', 'Hailey Bieber', 'Travis scott', 'Sofia Richie', '*Rob Kardashian', '*Kourtney Kardashian', 'Matt Kemp', 'Harry Styles', 'Drake', 'Jaden Smith', 'Lamar Odom', 'Trina', 'James Harden', 'Jordan Craig', 'Scott Dissick', 'Blac Chyna']

Class 1: ['MGK', 'Kris Humphries', 'Nick Lachey', '*Kim Kardashian', 'Miles Austin', 'Gabriel Aubrey', 'Larsa Pippen', 'Cristiano Ronaldo', 'Future', 'Amber Rose', 'Kaia Gerber', 'Kanye West', 'Ray J', 'Michael Copon', 'Ciara', 'Ariana Grande', 'John Mayer', 'Travis Barker', 'Nick Cannon', 'The Game', 'Damon Thomas', 'Reggie Bush', 'Pete Davidson', 'Megan Fox']
```
This partition was really odd to look at knowing what we know about pop culture and how these people actually cluster as a community in real life...Work in progress...

[I am still working on this...]


-------------------------------

## Sources
Marquina, S. (2021, October 13). Khloe Kardashian's dating history: Every rapper and athlete she's romanced. Us Weekly. Retrieved June 21, 2022, from https://www.usmagazine.com/celebrity-news/pictures/every-rapper-and-athlete-khloe-kardashian-has-dated-w440216/rashad-mccants-w440237/ 

Team, P. S. (2022, March 2). Kim Kardashian's full dating history: Ex-husbands, boyfriends and Flings. Page Six. Retrieved June 21, 2022, from https://pagesix.com/article/kim-kardashian-dating-history-ex-husbands-boyfriends-flings/ 

YouTube. (2018). YouTube. Retrieved June 21, 2022, from https://www.youtube.com/watch?v=u0aEqlbkPmU. 
