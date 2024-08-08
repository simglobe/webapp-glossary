# Introduction

Simglobe is a macroeconomic simulator in which players act as a policymaker who aims to maximize growth while ensuring economic stability. Although the real economy is very complex and real governments make a lot of policy decisions, the game aims to strip these economic dynamics to its core in order for players to learn for themselves how an economy works.

## *Game Scenario*

At the start, depending on the lecturer, you are given the choice or assigned a country. A country can be categorized according to their income and population. Each dimension has three tiers, high, medium, and low, giving us in total 9 types of country.

As a policymaker, you are given five tools to work with to control your economy: Interest rate, VAT, Corporate Tax, Government Spending, and Tariffs. There will be a range in which you will be able to adjust these policies.

The dynamics of the different types of countries and policies will be discussed later. For now it suffices to know there will be a difference.

## *How to win*

You will be playing against other countries. Your goal is simple: To be the country with the highest approval rating.

What is the approval rating? It is meant to represent the amount of support you get from your citizens, and it has four components:

* Real GDP growth

* Inflation rate

* Unemployment rate

* Fiscal balance (% of GDP)

The approval rating scales from 0 to 100, and each component has equal weights. This means that to achieve an approval rating of 100, you must achieve max scores for all four components. There will be specific criterias in order to reach the max score of the game, and they depend on the type of country the players are playing. The general objectives, however, are:

* Maximize real GDP growth 

* Keep inflation low

* Minimize unemployment rate

* Maximize fiscal surplus

With some economic knowledge, it can be seen that each goal can preclude one another. This will be discussed later on.

One further note is that this game is not a zero-sum game. Players can influence each other's results through international trade and finance, but on the whole does not directly compete with each other. This will also be left for later sections.

# Navigation

# Model overview

Simglobe itself is composed of three different parts that interact with each other: Demand-Supply, Public Sector, and Trade. Demand-Supply is the core of the model which determines Nominal GDP and Inflation, while Public Sector provides a constraint on Government Spending, and Trade allows countries interact with each other, on goodwill or with malice. 

## *Demand-Supply* 

Demand-Supply is the standard AD-AS model, where demand is presented by Income, and supply Output. Income is the identity Y \= C+G+I+(X-M), where the growth of consumption, investment, and imports are based on last-year Nominal GDP growth, adjusted for the effect of inflation, debt, and interest rate. Output, on the other hand, uses the production function whose result grows at a rate which is the sum of growth rate of factors of production. Labor growth is exogenous, technology growth is moderated by tariffs to simulate tech spillover, diffusion and competition, and capital stock grows by net of investment and depreciation, the latter being given. 

Changes in Income-Output represent shifts in the AD-AS curve, resulting in changing Nominal GDP and price level. 

## *Public Sector* 

Public sector is the second part of the model which is created to limit the power of government spending. It details the tax revenues from VAT, corporate tax and tariffs, and government spending. Each turn, fiscal balance is calculated which will add to or be deducted from last-year government debt. Low government debt will reward players with investment growth, while high debt will punish it, and the punishment will be much larger than rewards. 

## *Trade*

Trade is the last part of the model which shows the current and capital account of the country. In terms of current account, exports grow based on how cheap the currency is relative to other currencies, while imports grow based on how expensive the currency is relative to other currencies. For capital account, net capital flow increases or decreases depending on how low or high the interest rate is relative to global average. Exchange rate, which represents the value of the currency, fluctuates based on exports growth relative to import growth and net capital flow. 

# Policy

## *Interest rate*

Interest rate, which represents monetary policy, affects mostly the Aggregate Demand, Inflation, and Exchange Rate. 

* When the interest rate is increased, the price of loans increases which decreases consumption and investment, and vice versa. 

* The interest rate also has a direct effect on inflation. When the interest rate increases, inflation decreases.

* It also affects the attractiveness of investment in the economy. An interest rate increase results in higher returns for foreign investors. If the interest rate is higher relative to the global interest rate, which is the average interest rate of all economies, then there is a positive net capital flow. To invest in an economy, foreign investors use the currency of that economy; the demand for that country’s currency therefore increases as foreign investment increases, and the currency appreciates. As the value of currency is displayed as relative to USD, this means the number shown will decrease. 

It is advised that beginners adjust the interest rate by 1% at a time. 

## *Government spending*

Government spending is shown as a percentage of last-year Nominal GDP, and is a part of the Aggregate Demand equation, which means it has a direct effect in lifting the economy. It is, however, limited by government debt. Players are advised to keep government debt below 60% to avoid punishment to investment. 

It is advised that beginners adjust the government spending by 2-5% at a time. 

## *VAT and Corporate Tax*

VAT and Corporate Tax respectively affect consumption and investment. An increase and decrease of these tax rates will lift and depress the growth, to the point of being negative, of consumption and investment. 

It is advised that beginners adjust the VAT and Corporate Tax by 5% and 10% at a time.

## *Tariffs*

Tariffs affect imports. An increase or decrease of tariffs will lift and depress the growth, to the point of being negative, of imports.

It is advised that beginners adjust the Tariffs by 2-4% at a time. 

# Scoring

## *General rules*

The final score of the game is Approval Index, which is made up of four components: 

* Real GDP growth 

* Inflation rate

* Unemployment rate

* Fiscal balance (% of GDP)

The Approval Index and its components range from 0 to 100, and each component will have equal weights. This means to get 100 Approval Index, players must get 100 for each component. To do so, players need to cross a certain threshold, or keep themselves inside a certain range. These thresholds or ranges are different for different groups. For example, Thailand, a … income and … population country, has to fulfill the following criteria to get max Approval Index:

* Real GDP growth ≥ xxx

* 0 ≤ Inflation rate ≤ 

* Unemployment rate ≤ 

* Fiscal balance (% of GDP) ≥

Note that among these four components, the threshold is also its minimum value. This means that the minimum unemployment of Thailand is xxx. 

Furthermore, the thresholds and ranges for getting 0 for each component are also defined. In the case of Thailand, they are:

* Real GDP growth ≤  xxx

* Inflation rate ≤ , or ≥

* Unemployment rate ≥ 

* Fiscal balance (% of GDP) ≤

Within these thresholds, score is scaled linearly. As Real GDP growth varies from xxx to xxx, its score linearly scales from 0 \-100. The resulting score for some Real GDP growth are summarized in the following table:

## *Note on Inflation rate*

* Inflation rate has a “Goldilock zone” in which players attain the max score (For Thailand, xxx to xxx)

* Score generally scales much more quickly in deflation (i.e. negative inflation rate) (under the Goldilock zone) than in high inflation (above the Goldilock zone)

## *Note on Unemployment rate*

Unemployment rate has a minimum value, which is also the threshold at which players receive full score for this component. 

# Country types

In SimGlobe, countries are categorized based on their real life GDP per capita and population into three levels of high, medium, and low, resulting in a total of 9 types of country. Each of these types will have a unique set of parameters undisclosed to the players and can be configured by the room master. Additionally, each type of country will also have a unique set of thresholds and range of Approval Index components which are disclosed to the players.  

Although the parameters are undisclosed, here is a rough guide of the dynamics of each type of country, moving from low to high on the two dimensions: 

# Game flow

The flow of the game will be as followed:

* When the students enter a game room, they will be asked to pick a country or be assigned a country by the room master. Players will wait until all have entered the room, or when the room master manually decides to begin the game.   
* As the game begins, players will then make the policy decision for each round. All the information needed to make the decision are summarized in the dashboard. When detailed information about a particular variable is needed, players click on the dashboard to show the variables in the detailed panel.   
* Players will play for 8 rounds with the aim to maximize the Approval Index in round 8\. One particular mark players need to pay attention to is Round 4, where the Election happens. For you to be elected, your Approval Index needs to surpass  
* where the Approval Index needs to surpass 50 as a proxy for election. By not reaching 50, players will incur a punishment 

# Economic concepts 

# Shortcomings

Players new to economics may mistake SimGlobe for how the economy works. The game is only a model, and therefore subject to extensive simplification in order to extract the core economic dynamics and present them in a digestible manner. The following details what aspects of the economy that it does not capture:

* There are no shocks built into the game, either from the supply side such as an oil shock, or from the demand side such as a financial crisis. This also means there is in general no business cycle involved. 

* Labor growth is exogenous, which does not reflect the complex inner working of the labor market and demographics. Technology growth is also exogenous which is not true as it depends on how much corporations and governments invest in R\&D, and how effective they are at generating innovations. 

* Unemployment, boiled down to two rather uncomplicated laws, does not reflect the micro-economic dynamics which define its variation. 

* Environmental impact is entirely ignored. It is capable of imposing a significant cost on economic growth and stability in real life.  

Students can use the game as a simplified mental model of the economy, but they must also be aware of other aspects or nuanced interactions that the game decided to strip off itself to have a comprehensive understanding of the economy and the influence of policies. 

# Troubleshooting

This is a manual on how to quickly troubleshoot and fix your economy. It is only intended for emergencies; players should go through the Basic and Master Tutorial, as well as the Help Page to understand the dynamics of the game. 

When making policy decisions, players must choose (1) in what direction, and (2) how much should policies be adjusted. 

* Direction: The following table briefly explains the immediate underlying cause of each potential issue and their solution. Note that this only shows the primary effect; players need to take into account side effects.

| Indicators | Status | Cause | Recommendation |
| :---- | :---- | :---- | :---- |
| Real GDP growth | Low/Negative | Low Nominal GDP growth | Decrease interest rate Decrease tax rates Increase spending Increase tariffs |
|  |  | High inflation rate | Refer to Inflation rate |
| Inflation rate | Too high | Demand growth is weaker than supply growth | Increase interest rate  Increase VAT  Decrease corporate tax rate Decrease spending Increase tariffs |
|  | Too low | Demand growth is stronger than supply growth | Opposite of high inflation rate |
| Unemployment  | Too high | Low Real GDP growth | Refer to Real GDP growth |
| Fiscal balance  | Too negative  | Spending more than tax revenues | Increase tax rates Decrease spending |

* Amount: The following table is a recommendation how much the players should adjust their policy each round, if they do decide to. Note that the below recommendation is larger than the recommendations in the *Policy* section as players need to act in emergencies.

| Policy | Adjustment |
| :---- | :---- |
| Interest rate | 2% |
| VAT and Corporate tax rate | 10% |
| Government Spending | 5% |
| Tariff | 5% |

