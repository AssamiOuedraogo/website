---
categories:
- ""
- ""
date: "2017-10-31T22:42:51-05:00"
description: Nullam et orci eu lorem consequat tincidunt vivamus et sagittis magna
  sed nunc rhoncus condimentum sem. In efficitur ligula tate urna. Maecenas massa
  sed magna lacinia magna pellentesque lorem ipsum dolor. Nullam et orci eu lorem
  consequat tincidunt. Vivamus et sagittis tempus.
draft: false
image: pic07.jpg
keywords: ""
slug: beer
title: Top 25 Beer consumption
---

```{r beer_plot}
# YOUR CODE GOES HERE
drinks%>%
arrange(desc(beer_servings))%>%
head(25)%>% 
ggplot(aes(y= reorder(country,beer_servings),
                  x=beer_servings,
                  fill=country))+
  geom_col()+
  theme(legend.position = "none")+
  labs(title = "Top beer consumiing countries")

```