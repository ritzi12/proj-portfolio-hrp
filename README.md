# Hierarchical Risk Parity - Portfolio Optimisation Technique

In this project we explore the method of HRP for porfolio composition which has well diversified risk. And we compare it's performance against conventional portfolio optimisation technique such as Markowitz Mean-Variance(MVP) Portfolio. 

**Algorithm** -  The HRP algorithm has been taken from the paper [Marcos Lopez de Prado (2016)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2708678)

**Data** - The data has been extracted from *yahoo finance* . We select Nifty 500 companies and fetch their Closing prices for 2  yrs Jan-2020 to Dec-2021 . This is training dataset and test dataset is for 1 year Jan-2022 to Dec-2022

Introduction
In today's dynamic and interconnected financial markets, effective risk management is crucial for investors seeking to achieve optimal portfolio performance. Traditional portfolio allocation methods often fall short in capturing the complex relationships among assets, leading to suboptimal risk diversification. However, the Hierarchical Risk Parity (HRP) method offers a promising solution by leveraging the hierarchical structure of asset correlations to optimize risk allocation.

To understand the power of HRP, let's consider a real-life example. Imagine an investment firm managing a diverse portfolio comprising stocks from different sectors, bonds, and commodities. The traditional risk allocation approach, such as equal weighting or based on market capitalization, might not adequately capture the intricate interdependencies between these assets, leaving the portfolio vulnerable to concentration risk.

HRP is a new portfolio optimization technique developed by Marcos Lopez de Prado (2016). This model consist of the following three steps:

Hierarchical Tree Clustering: we take advantage of the relationship among financial assets (correlation) to create a hierarchical structure that can be plotted as a dendrogram. involves constructing a hierarchical tree using a clustering algorithm, which groups assets based on their pairwise correlations. For instance, stocks within the same sector might exhibit higher correlations, while bonds and commodities might form separate clusters.

Matrix Seriation: we sort the assets in the dendrogram minimizing the distance between leafs, Lopez de Prado called this process quasi-diagonalization.

Recursive Bisection: we split the weights along the dendrogram using naive risk parity (weights based on the inverse of asset’s risk) from the top of the tree to the leafs.The HRP method calculates allocation weights that prioritize clusters with low inter-cluster correlation and high intra-cluster correlation. By doing so, the method ensures that risk is distributed evenly across different levels of the hierarchy, mitigating the impact of potential sector-specific shocks or market-wide events.

The HRP method's advantages become evident when compared to traditional approaches. Unlike a market-capitalization-weighted portfolio, which may heavily favor certain sectors or assets, HRP provides a comprehensive risk-based allocation that adapts to changing market conditions. It enables investors to dynamically rebalance their portfolios, ensuring risk is managed in an optimal and responsive manner.


## Results or Data Visualisations

###  Clustering and Dendogram of Stocks

![image](https://github.com/ritzi12/proj-portfolio-hrp/assets/80144294/6a58795d-0eab-4022-8b17-e158f4992bcb)

### Portfolio COmposition

![image](https://github.com/ritzi12/proj-portfolio-hrp/assets/80144294/dbfe18db-df4a-4111-9649-a2813ddc849f)

![image](https://github.com/ritzi12/proj-portfolio-hrp/assets/80144294/fee99c63-941f-4260-a289-4cfe88a5c68a)

### Cumulative Returns

![image](https://github.com/ritzi12/proj-portfolio-hrp/assets/80144294/9118772c-0cef-40dc-806a-9c07878625e9)

![image](https://github.com/ritzi12/proj-portfolio-hrp/assets/80144294/a5fb2e86-6619-4935-9efb-17d622e2e256)




