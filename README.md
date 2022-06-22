# Pop-Culture-Graphs


## Kardashian- Jenner Graph
I created this for myself, because I saw a TikTok and got very confused when someone tried to explain to me how connected everyone was from dating.

I used python, networkx, and pyviz to create this graph. The data comes from TV interviews were Kardashian-Jenner family has confirmed their relationships and rumors, from their own TV show, and numerous news articles. A list of sources can be found bellow.

So there are family, friends, rumored relationships, and confirmed relationships on the graph. The family is the bold color, friends are the pinkish red color, confirmed relationships/flings/hookups/marriages/etc are green, and rumors are yellow.

<img width="668" alt="Screen Shot 2022-06-22 at 12 10 24 PM" src="https://user-images.githubusercontent.com/37605496/175097247-7507bdd7-6b46-445c-8b68-994c6f595949.png">


(updated Jun. 22, 2022)


## Analysis

The network density is ```0.05628415300546448```, which is the ratio between actual edges versus all possible edges in the graph. The denser the network the closer to 1 the density is just to see how connected the graph is. 

The diameter of the graph is just 5, which is not suprising, because it is a very small graph. Hpwever that is the longest of all the shortest paths in the graph. So the diameter between the nodes that are farthest apart in the network is just ```5```. 

I also took the triadic closure which is a way to find triangles, like if a and b both know c then a and b should know of each other. For this graph the triadic closure is ```0.18726114649681527```. Notice how the density is lower than the closure so that means there are a lot of triangles that exist in this graph. But clearly with cheating and everything we know about this network I wonder what that could say about this network....

Clearly some of the most important parts of this graph is knowing the centrality basically who is the most important or if not has the most edges. This is the top 20 in just degrees: 
```
Top 20 nodes by degree:
('*Kim Kardashian', 24)
('*Kendall Jenner', 15)
('*Khloé Kardashian', 14)
('*Kris Jenner', 13)
('*Kylie Jenner', 12)
('*Kourtney Kardashian', 10)
('*Rob Kardashian', 7)
('Travis scott', 5)
('Blac Chyna', 5)
('Kanye West', 5)
('Future', 5)
('MGK', 4)
('Pete Davidson', 4)
('Tristan Thompson', 4)
('Drake', 4)
('Jordyn Woods', 3)
('Justine Sky', 3)
('Tyga', 3)
('Sofia Richie', 3)
('Justin Beiber', 3)
```
Which seems correct from everything we know about the Kardashian-Jenner family and the fact that this was a network of their relationships. Also, I took the betweeness centrality, which is nodes that connect clusters of the network. The higher the number the more likely these people broker information within this graph to different clusters. The top 20 nodes in that analysis:
```
Top 20 nodes by betweenness centrality:
Name: *Kim Kardashian | Betweenness Centrality: 0.5073894717962517 | Degree: 24
Name: *Kendall Jenner | Betweenness Centrality: 0.22984126984126985 | Degree: 15
Name: *Kris Jenner | Betweenness Centrality: 0.2214689265536723 | Degree: 13
Name: *Khloé Kardashian | Betweenness Centrality: 0.21686283741368492 | Degree: 14
Name: *Kylie Jenner | Betweenness Centrality: 0.14413326159088874 | Degree: 12
Name: *Kourtney Kardashian | Betweenness Centrality: 0.09620258272800651 | Degree: 10
Name: Pete Davidson | Betweenness Centrality: 0.06021657250470807 | Degree: 4
Name: MGK | Betweenness Centrality: 0.036803874092009685 | Degree: 4
Name: Blac Chyna | Betweenness Centrality: 0.03581091381938839 | Degree: 5
Name: Travis Barker | Betweenness Centrality: 0.03283965563626579 | Degree: 3
Name: Kanye West | Betweenness Centrality: 0.030467895256030858 | Degree: 5
Name: Tristan Thompson | Betweenness Centrality: 0.02353197022688548 | Degree: 4
Name: Tyga | Betweenness Centrality: 0.016987489911218727 | Degree: 3
Name: *Rob Kardashian | Betweenness Centrality: 0.015554434579858308 | Degree: 7
Name: Larsa Pippen | Betweenness Centrality: 0.014991480584700914 | Degree: 3
Name: Amber Rose | Betweenness Centrality: 0.009041789973993363 | Degree: 3
Name: Travis scott | Betweenness Centrality: 0.008192090395480226 | Degree: 5
Name: Kaia Gerber | Betweenness Centrality: 0.006770244821092279 | Degree: 2
Name: Drake | Betweenness Centrality: 0.00633844498251278 | Degree: 4
Name: Future | Betweenness Centrality: 0.006238005560039459 | Degree: 5
```

I also tried to see if I could detect communities, but I don't think I choose the right partition for this network. Will definetely keep working on this. But currently it looks like this: 
```
Class 0: ['Reggie Bush', 'Justine Sky', 'Corey Gamble', '*Kim Kardashian', 'Kris Humphries', 'Matt Kemp', 'French Montana', 'Devin Booker', 'Drake', 'Todd Waterman', 'Robert Kardashian', 'Travis scott', 'Alfred M. Garcia', '*Kendall Jenner', 'Michael Copon', 'Ben Simmons', 'Anwar Hadid', '*Kourtney Kardashian', 'Jordyn Woods', 'Amber Rose', '*Rob Kardashian', 'Ray J', 'Nick Cannon', 'Tyga', 'James Harden', 'Jaden Smith', 'Trina', 'Future', 'Cristiano Ronaldo', 'OJ Simpson', 'Harry Styles', 'Travis Barker', 'Caitlyn Jenner', 'Blac Chyna', 'Lamar Odom', 'Cesar Sanudo', 'Nick Lachey', 'Gabriel Aubrey', 'Jordan Craig', 'The Game', 'Younes Bendjima', 'John Mayer', 'Damon Thomas', 'Hailey Bieber', 'Larsa Pippen', '*Kylie Jenner', '*Kris Jenner', 'Ciara', 'Justin Beiber', 'Sofia Richie', 'Kanye West', '*Khloé Kardashian', 'Tristan Thompson', 'Derrick Ward', 'Miles Austin', 'Scott Dissick']

Class 1: ['Ariana Grande', 'Pete Davidson', 'Megan Fox', 'MGK', 'Kaia Gerber']
```
This partition was really odd to look at knowing what we know about pop culture and how these people actually cluster as a community in real life...Work in progress...

```
Modularity Class 0 Sorted by Eigenvector Centrality:
Name: *Kim Kardashian | Eigenvector Centrality: 0.4252184847860199
Name: *Kendall Jenner | Eigenvector Centrality: 0.3452193086157082
Name: *Khloé Kardashian | Eigenvector Centrality: 0.33475083979804626
Name: *Kylie Jenner | Eigenvector Centrality: 0.32987690504049955
Name: *Kris Jenner | Eigenvector Centrality: 0.3126353371571706
```



[I am still working on this...]


-------------------------------

## Sources
Marquina, S. (2021, October 13). Khloe Kardashian's dating history: Every rapper and athlete she's romanced. Us Weekly. Retrieved June 21, 2022, from https://www.usmagazine.com/celebrity-news/pictures/every-rapper-and-athlete-khloe-kardashian-has-dated-w440216/rashad-mccants-w440237/ 

Team, P. S. (2022, March 2). Kim Kardashian's full dating history: Ex-husbands, boyfriends and Flings. Page Six. Retrieved June 21, 2022, from https://pagesix.com/article/kim-kardashian-dating-history-ex-husbands-boyfriends-flings/ 

YouTube. (2018). YouTube. Retrieved June 21, 2022, from https://www.youtube.com/watch?v=u0aEqlbkPmU. 
