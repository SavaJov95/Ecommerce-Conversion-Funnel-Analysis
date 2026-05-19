<div align="center">
    <h1>Ecommerce Conversion Funnel Analysis</h1>
</div>

<h2 align="center">Project Background</h1>

**UrbanHive Commerce** is a rapidly growing e-commerce company focused on affordable lifestyle products, including home office accessories, fitness equipment, and everyday tech gadgets. The company primarily targets younger digital-first consumers through online campaigns, social media advertising, and mobile-driven shopping experiences.

Over the last year, UrbanHive Commerce expanded aggressively into new digital acquisition channels in an attempt to increase market share and accelerate customer growth. While website traffic has increased significantly, company executives have become concerned about declining conversion efficiency and inconsistent customer purchasing behavior across products and marketing channels.

To better understand customer behavior and improve operational decision-making, the company has collected detailed event-level interaction data across the entire customer journey — from initial product views to completed purchases. 

The major goals of this deep-dive analysis were to measure the effectiveness of the marketing channels, identify drop-off points in the purchasing process and understand customer purchasing patterns to assist the company's marketing team.

The complete analysis, including visualizations, is created in Jupyter Notebook and can be found [here](funnel_analysis.ipynb).
</br>
</br>
<h1 align="center">Data Structure</h1>

Dataset used for this analysis can be found here: [dataset](dataset/user_events.csv).  

![Data Structure](images/Data%20Structure.png)

<h1 align="center">Executive Summary</h1>

Analysis reveals that the **lower stages of the conversion process (checkout and payment) are highly optimized**, showing minimal user drop-off. However, **the primary bottleneck occurs at the top of the funnel**, where only 31.2% of users proceed from product views to adding items to the cart. This indicates that improving conversion in these initial stages represents the biggest optimization opportunity.  
**Organic traffic** emerged as the strongest overall revenue driver among marketing channels, generating both **high traffic volume and strong conversion performance**. **Email traffic delivered the highest revenue efficiency per visitor**, while **social traffic consistently underperformed in conversion quality despite generating substantial volume**.  
The product portfolio shows balanced performance, with **Product 205** demonstrating the strongest balance between customer attention and conversion efficiency.  
Customer activity peaks during **Sunday and Monday evenings**.  
These findings suggest opportunities for optimizing campaign scheduling and marketing timing strategies and will be further explored in the following sections, along with recommendations for future actions.

<h1 align="center">Insights Deep-Dive</h1>
<h2>1. Conversion Funnel</h2>

We analyzed a dataset consisting of data from the last 30 days. This data represents the number of users at different stages of the funnel. Evidently, many users do not overcome the initial obstacle, abandoning our platform without even adding a product to their cart.

| Funnel Stage | Users |
| ------------ | ----: |
| Page View    | 4268  |
| Add to Cart  | 1332  |
| Checkout     |  951  |
| Payment      |  768  |
| Purchase     |  708  |
 
One of the most important parts of our analysis was to determine the conversion rates between each stage in our behavioral funnel.  
The initial stage, from **page view to product added to cart**, exhibits a **conversion rate of 31.2%**. That indicates that, approximately one-third of users who view a page, proceed to add a product to a cart, making this clearly the stage with the **highest user loss in the funnel**. One reason could be a high number of low-quality users who are merely "passersby" on our platform. We need high-intent users whose goal is to complete a transaction.    
After successfully adding a product to a cart, **71,4% of users proceed to the checkout phase**, indicating no significant "cart hesitation" problems such as complex checkout flows, unexpected costs, or required registration.  
Further along the funnel, conversion rates increase, with **80.8% of users in the checkout stage providing payment information**. Subsequently, **92.2% of those users complete the purchase**, suggesting our payment flow is well-optimized and robust, free from bugs and trust issues.
**The overall conversion rate for the funnel is 16,6%**, meaning approximately one in six users on our platform purchases a product.  
There appear to be no major issues in the lower stages of the funnel, these are performing quite well. Therefore, our primary goal should be to improve the first-stage conversion and transition more users to subsequent stages. 

![Conversion Rates in the Funnel](images/Conversion%20Rates.png)

<h2>2. Marketing Channel</h2>

Our dataset comprises four acquisition channels: organic search, paid advertisements, email links, and social media posts (e.g., Facebook, Instagram, TikTok).
The chart below highlights some interesting findings.  
**Social media platforms** excel at attracting users to our websites and apps. However, these users tend to be low quality, resulting in a **very low purchase rate of only 6,7%**. This suggests that while our social media content is entertaining and engaging, it yields no concrete results.  
The majority of users arrive via **organic search**, indicating that our search engine optimization effectively guides users to our platforms. With an **overall conversion rate of 17,1%**, we can be satisfied with this marketing channel's contribution, health, and scalability. 

![Marketing Channel Conversion](images/Marketing%20Channel%20Conversion.png)

**Paid ads have an even better view-to-purchase ratio - 21,1%**, meaning that 1 out of 5 users who click an advertisement banner buy our products.   
Users who come through **email** links, whether from newsletters or promotional emails, appear to be **high-intent users, with 33,9% purchase rate**. Although email, as a digital marketing channel, is not as efficient for us in attracting many users, every third user who comes from this acquisition channel becomes a customer. This indicates that email is a strong performer in bringing high-quality traffic to our platforms.  
All of the above indicates that a marketing channel with higher generating power does not necessarily lead to higher conversion efficiency.

![Drop-off Rate](images/Drop-off%20Rate.png)

Users who come from social channels are specific. Mostly younger generations, who are intensive social media users, impulsively browse our platform and do not have high purchase intent. They don't know our brand and lack the trust needed to make transactions on unfamiliar territory. I wanted to investigate at which point in the funnel social users drastically drop off, as there was a possibility that checkout or payment presented a problematic stage for this group of users.  
The most important insight from this analysis is the **severe early-stage users drop-off rate** (86,4%) observed, especially in the social traffic channel. A lot of users who originated from organic search (67,1%) or paid ads (62,8%) also fell at the first hurdle. In contrast, the email channel is doing an excellent job with only 37,1% view-to-cart drop-off rate. Later stages of the funnel are much more successful at user retention.

![Marketing Channel Revenue](images/Channel%20Revenue.png)

Users acquired through social media demonstrate:
- Very high abandonment between page view and add to cart
- The weakest overall conversion efficiency
- The lowest revenue generated per visitor

The data suggests that social traffic primarily drives awareness and engagement, attracting a large volume of users, most of whom exhibit low purchase intent. 
Drop-off analysis indicates that the company's checkout and payment experience is generally well optimized across all acquisition channels. The primary business challenge lies earlier in the customer journey — specifically in attracting and engaging users with genuine purchase intent. 
Among all channels:
- Email traffic delivers the highest-quality customers
- Organic traffic provides the strongest balance of scale and revenue generation
- Paid advertising demonstrates promising monetization efficiency
- Social traffic underperforms significantly in conversion quality despite strong visitor volume

The findings suggest that **future business growth will depend less on increasing raw traffic and more on improving acquisition quality and top-of-funnel engagement strategies.**

<h2>3. Product Performance</h2>

This analysis indicates that product performance differences are relatively balanced across the portfolio, suggesting stable overall product health.  
Product 205 demonstrates the strongest balance between customer attention and conversion efficiency, positioning it as the most commercially effective product in the catalog. Meanwhile, products such as 201 and 404 generate strong visibility but underperform in conversion efficiency, indicating potential optimization opportunities related to pricing, positioning, or product page experience. Product 102 potentially presents a hidden growth opportunity; it currently receives insufficient attention but demonstrates strong conversion rates when 
engaged.  
Overall, **the portfolio appears diversified, with no significant dependency on a single product for conversion performance**.

![Product Performance through the Funnel](images/Product%20Performance%20through%20the%20Funnel.png)

From this matrix, it's clear that most products generate very high revenue through organic traffic, with the exception of product 102, which is lagging. There is an excellent channel-product fit, particularly for **products 101, 201 and 404, where the acquisition channel is well-aligned with the product pages**, leading to strong performance.  
Conversely, **the social channel consistently underperforms compared to other channels across most products**. While products 101 and 205 show solid performance, other products underperform. Products 102, 201 and 404 perform particularly poorly, generating almost four times less revenue than through organic traffic.  
The paid-ads channel shows very consistent performance across the product portfolio. It is generally balanced, with the exception of product 201, which has the best conversion rate. We could analyze the reasons for this success and use it as a playbook for scaling other products.  
The email audience does not react evenly across all products; products 102 and 205 are favorites among email traffic. We should investigate whether there is a special product affinity driving this uneven selectivity.  
Total revenue is similarly distributed across products, with differences falling within normal limits. **The only product consistently falling behind is product 102, even in organic traffic. Products 101 and 205 stand out for their consistency across every acquisition channel, making them our most stable products. Product 201 responds well to intent-driven channels (Organic, Paid) but poorly to push channels (Email)**. This suggests it's a product purchased when users actively search for it, rather than when it is merely presented to them.  
Overall, we can conclude that **our product portfolio has solid performance and is well-optimized. The main focus should be on optimizing acquisition channels.**

![Product Performance by Marketing Channel](images/Product%20Performance%20by%20Marketing%20Channel.png)

<h2>4. Time Analysis</h2>

Overall, Sunday and Monday exhibit the strongest purchase activity, particularly **Sunday evening and Monday afternoon/evening**. Users show significantly higher purchase intent during weekends, likely due to relaxation on non-working days. Sunday maintains activity throughout the entire day, a pattern not observed on other days. In contrast, mid-week purchase activity is weaker and more fragmented, lacking clear peaks. User activity during the workweek is much less concentrated, with Thursday appearing as a "dead" day at almost all hours.   
Evening hours generally outperform daytime hours, with **activity peaking after 19:00, primarily on Sunday and Monday**. Additionally, **some days show higher user purchase activity between 13:00 and 17:00**. This suggests customers tend to make purchases after working hours and their daily duties. 
Some isolated early-morning activity spikes appear in the dataset, although additional data would be required to determine whether these represent stable behavioral patterns or short-term anomalies.  
These findings provide actionable opportunities for campaign scheduling, retargeting optimization, and more efficient allocation of marketing activity throughout the week.

![Day and Hour Purchase Peak](images/Day%20&%20Hour%20Purchase%20Peek.png)

<h1 align="center">Recommendations</h1>
<h2>1. Conversion Funnel</h2>

Based on the funnel analysis, the largest drop-off occurs between product views and add-to-cart actions. To address this, A/B testing is recommended on product pages, focusing on elements such as:
- pricing presentation,
- product descriptions,
- images, and
- call-to-action design.  

The objective is to identify variations that increase user engagement and improve the add-to-cart rate. 
Lower funnel stages are performing well, exhibiting excellent conversion rates (80%+); consequently, no changes to the UX or website optimization are recommended for these areas. 

<h2>2. Marketing Channels</h2>

<h3>Reevaluate Social Media Targeting</h3>

While the social channel generates high visitor volume, it suffers from very low conversion efficiency, indicating weak purchase intent. The largest drop-off occurs at the very beginning of the funnel. To address this, we should focus on: 
- Introducing retargeting campaigns for engaged visitors
- Improving alignment between advertisements and landing pages
- Testing more purchase-oriented ad creatives

Additionally, an aggressive email capture popup could be implemented for these high-volume social visitors. Our data proves that once they are on our email list, they are far more likely to purchase later.

<h3>Scale Email Marketing Efforts</h3>

Email traffic demonstrates the strongest conversion efficiency and highest revenue per visitor across all channels. We need to make sure it stays successful, so we should invest in:
- Expanding personalized email marketing campaigns
- Introducing product recommendation emails
- Building customer loyalty and retention programs
- Increasing post-purchase engagement campaigns

<h3>Continue Expanding Organic Acquisition</h3>

Organic channel delivers the highest overall revenue while maintaining healthy funnel performance and stable user purchasing behavior. My suggestions are:
- Continue SEO optimization efforts
- Expand high-performing content marketing strategies
- Improve organic landing page experience

<h3>IMPORTANT LIMITATION</h3>

The absence of marketing cost data is a critical limitation of this analysis. This information is essential to accurately determine the profitability of different acquisition channels. Without it, we cannot calculate key metrics such as Return on Ad Spend (ROAS) or Customer Acquisition Cost (CAC), which are necessary for comparison with Customer Lifetime Value (LTV). 
**Consequently, it is impossible to ascertain whether a marketing channel is truly profitable, or if scaling a particular channel would improve overall profitability.**  
This is a crucial consideration for future analyses.

<h2>3. Product Performance</h2>

**Products such as 201 and 404** attract significant user attention but convert less efficiently compared to other products. Product pages for these items should be reviewed for potential issues related to pricing, messaging, product descriptions, reviews, or overall purchase experience, **making them ideal candidates for A/B testing.**  
**Products 101 and 205** demonstrate the strongest balance between traffic share and conversion efficiency, while also generating the highest revenue. They are our most stable products, and we should **increase the marketing budget to keep pushing them further capitalize on their success.**  
**Product 102** performs poorly in terms of revenue and visibility but shows high potential with its superb conversion. The marketing team should **increase promotional exposure** for this product through paid campaigns, featured placements, and email marketing.

<h3>IMPORTANT LIMITATION</h3>

Revenue analysis by product is not truly representative without product price information. The potential for significant price differences between products completely alters the interpretation.

<h2>4. Time Analysis</h2>

<h3 >Email Campaigns</h3>
We should send emails 1-2 hours before the peak period, not during it. Users need time to open, read, and convert. Monday at 19h is an ideal time.

<h3>Paid-Ads Scheduling</h3>
Build two bid-adjustment windows:

- Monday: Increase budget by 30–40% between 7 PM and 11 PM.
- Sunday: Evenly increase the budget from 10 AM until the end of the day.

<h3>Thursday Options</h3>
Two possible approaches are: test a Thursday-only deal to "wake it up", or simply lower the Paid Ads budget on Thursday and reallocate it to Monday/Sunday. The latter is a quick win.