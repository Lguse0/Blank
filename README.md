# 🎬 Global Cinema: What 75 Years of Movies Reveal About Hollywood, Money, and Culture

**Dataset:** [Global Movies Dataset 1950–2026](https://www.kaggle.com/datasets/suhanigupta04/global-movies-dataset-19502026) by Suha Gupta on Kaggle  
**Tool:** [Malloy](https://www.malloydata.dev/) + DuckDB  
**Rows:** 100,000 films across 75 years and 10 countries  

---

## 🤔 The Question That Started It All

I've always been fascinated by movies — not just as entertainment, but as a reflection of culture, economics, and global storytelling. When I found a dataset spanning 75 years of global cinema, I had one burning question:

> *"Has Hollywood always dominated global cinema, or have other countries been quietly catching up — and does spending more money actually guarantee a better film?"*

What followed was a deep dive that completely changed how I think about the film industry.

---

## 📊 What I Found

### 1. The 1950s Were the Golden Age — And Ratings Have Never Recovered

The first thing I queried was movie production and ratings by decade. I expected ratings to improve over time as filmmaking matured. Instead, the opposite is true.

![by_decade query results](screenshots/Screenshot_2026-04-23_at_10_15_12 PM.png)

The 1950s had the highest average IMDb rating at **6.81** and the highest average ROI at **181.8%**. Every decade since has seen ratings decline slightly, bottoming out in the 1980s at **6.697** before a modest recovery. The 2020s are still incomplete, but are tracking at 6.724. The lesson: more movies doesn't mean better movies — the classic era set a quality bar that has never been matched.

---

### 2. No Country Dominates — The Playing Field Is Surprisingly Level

I assumed the USA would lead in both volume and quality. The data told a different story entirely.

![by_country query results](screenshots/Screenshot_2026-04-23_at_10_15_23 PM.png)

India leads in movie count with **10,165 films**, followed closely by the UK (10,095), Italy (10,059), and Germany (10,022). The USA ranks 9th with just **9,877 films**. Even more surprising — the average ratings across all countries are nearly identical, ranging from 6.725 to 6.755. Italy leads with **6.755**, while South Korea sits lowest at **6.726**. Global cinema is far more evenly distributed than the Hollywood-centric narrative suggests.

---

### 3. Fantasy and Genre-Blending Films Rate Highest — But Animation Earns the Most

I was curious whether certain genres consistently outperform others in both critical and audience reception.

![top_genres_by_rating results](screenshots/Screenshot_2026-04-23_at_10_15_37 PM.png)

Fantasy|Adventure|Sci-Fi combinations top the ratings chart with an average IMDb score of **8.083** and a metascore of **82.8**. Drama|Comedy|Fantasy and Crime|Fantasy|Drama follow closely. These are all multi-genre blended films — pure single-genre films rarely reach the top.

But when I looked at revenue and ROI, a completely different picture emerged:

![top_genres_by_revenue results](screenshots/Screenshot_2026-04-23_at_10_16_36 PM.png)

Animation|Comedy|Adventure leads with a stunning **639% average ROI** — far ahead of any other genre combination. The genres that audiences rate highest are not the same genres that make studios the most money. There is a real and measurable gap between critical quality and commercial success.

---

### 4. The Franchise Myth — Original Films Actually Outperform

One of my biggest surprises came from the franchise vs. original film comparison.

![franchise_vs_original results](screenshots/Screenshot_2026-04-23_at_10_18_15 PM.png)

Conventional wisdom says franchise films are safer bets. The data disagrees. Original films (franchise_flag = 0) outperform franchise films on every metric: higher average rating (**6.741 vs 6.714**), higher average revenue (**$133.8M vs $130.9M**), higher average ROI (**177.3% vs 175.1%**), and higher popularity (**80.1 vs 79.9**). Original films also account for the vast majority of blockbusters — **18,581 vs 3,947**. Studios betting big on franchises may be leaving money on the table.

---

### 5. Drama Wins Awards, But Animation Wins at the Box Office

Looking at awards by genre revealed another fascinating tension.

![awards_by_genre results](screenshots/Screenshot_2026-04-23_at_10_18_39 PM.png)

Drama dominates award season with **4,425 nominations and 1,652 wins**, followed by Documentary with **3,969 nominations and 1,533 wins**. Drama also carries the highest average rating of any single genre at **7.022**. Yet Drama is not among the top revenue or ROI performers. The films that win awards and the films that make money are almost entirely different films.

---

### 6. Streaming Platforms Are Nearly Indistinguishable

I expected Netflix or Disney+ to stand out clearly. Instead, the data showed something remarkable.

![by_platform results](screenshots/Screenshot_2026-04-23_at_10_17_53 PM.png)

All streaming platforms have nearly identical average ratings — Hulu leads at **6.755** and Peacock sits last at **6.718**, a difference of just 0.037 points across the entire platform landscape. This suggests that content quality is not a meaningful differentiator between streaming services — at least not as measured by IMDb ratings or audience scores.

---

### 7. Runtime Has Been Remarkably Stable For 75 Years

I expected movies to be getting longer. They aren't.

![runtime_by_decade results](screenshots/Screenshot_2026-04-23_at_10_17_10 PM.png)

Average runtime has stayed between **113.5 and 114 minutes** across every decade from the 1950s to the 2020s. Despite dramatic changes in technology, distribution, and storytelling, the two-hour movie has been the global standard for 75 years and shows no signs of changing.

---

### 8. The Greatest Films Come From Everywhere

The top 25 highest-rated films in the dataset score **9.8 on IMDb** and come from France, South Korea, Japan, India, Australia, the UK, Germany, and Italy — directed by Bong Joon-ho, Greta Gerwig, Denis Villeneuve, Sofia Coppola, Christopher Nolan, Martin Scorsese, Patty Jenkins, and Quentin Tarantino.

![top_rated_movies results](screenshots/Screenshot_2026-04-23_at_10_19_59 PM.png)

No single country or director monopolizes the top of the ratings chart. The best cinema in the world is truly global.

---

## 🗂️ Repo Structure

```
global-movies-malloy/
├── README.md                  ← This file
├── global_movies.csv          ← Full dataset (100,000 rows)
├── movies.malloy              ← Malloy source with all measures and queries
├── story.malloynb             ← Narrative notebook
└── screenshots/               ← Query result screenshots
```

## 🚀 How to Run This Yourself

1. Clone this repo
2. Install the [Malloy VS Code Extension](https://marketplace.visualstudio.com/items?itemName=malloydata.malloy-vscode)
3. Open `movies.malloy` in VS Code
4. Click **Run** above any query

---

## 🎯 So What? Who Should Care About These Findings?

These findings have real implications for multiple audiences. **Film studio executives and investors** should reconsider their franchise-first strategy — the data shows original films consistently generate higher ratings, revenue, and ROI than franchise sequels. **Streaming platform executives** at Netflix, Disney+, and others should note that content quality as measured by ratings is essentially identical across all platforms, meaning differentiation must come from exclusive content or user experience rather than average quality. **Independent filmmakers** can take encouragement from the finding that the USA does not dominate global cinema in volume or quality — the best films in this dataset come from everywhere, directed by a diverse global roster of talent. **Film funding bodies and cultural ministries** in countries building their domestic film industries should focus on Drama and Documentary genres, which consistently earn the highest ratings and the most awards recognition. Finally, **marketing executives** should pay close attention to the Animation|Comedy|Adventure finding — this genre combination delivers a 639% average ROI, far outpacing any other genre, suggesting significant underinvestment in animated features relative to their commercial potential.

---

*Analysis by Leah Guse | Built with [Malloy](https://www.malloydata.dev/) | Data from [Kaggle](https://www.kaggle.com/datasets/suhanigupta04/global-movies-dataset-19502026)*
