---
title: Stripe data explained and hit $6000 MRR
author_slug: adriaan
badge: "Monthly: May"
author: Adriaan van Rossum
image: /images/2020-05/woman-using-pc-and-android-phone-at-home-office.png
---

The monthly update of Simple Analytics will look a bit different than normal. This time I took screenshots of all data within the dashboard of Stripe and will comment on every single aspect of it. If you like graphs and numbers, this is your month!

We also hit a new milestone: \$6000 MRR. But you have lots of milestones if you switch between the number of paying customers, monthly recurring revenue, and annual recurring revenue. To me, the MRR is the most important metric of these three because I can see every moment if I'm still adding value compared to last month.

![Woman using pc and android phone at home office and looking at the public dashboard of Nomad List.com](https://assets.simpleanalytics.com/blog/github/2020-05-woman-using-pc-and-android-phone-at-home-office.png)

We use Stripe as our payment provider. It's a bit complex for our use case, but almost everything we want is possible in the end. Simple Analytics is located in The Netherlands and this comes with its tax requirements. If we would have a payment provider that also worked well with doing taxes, then that would be a huge benefit.

Back to their dashboard. I copied the main dashboard of Stripe and sliced all visible metric blocks into the images you see below. I didn't leave out any metric because I believe it's good to cover all aspects. Feel free to skip the ones you don't find interesting.

> This data shows 12 months from June 1, 2019, to May 31, 2020. The comparison with the previous 12 months is not completely fair because we don't exist for 2 years yet.

The first paragraph explains the metric, then comes the metric graph and numbers, and below that, I try to shed some light on the numbers regarding Simple Analytics.

## Gross volume

Gross volume is the total sales value. This number does include costs like fees, refunds, and disputes.

![Gross volume of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-01-gross-volume@2x.png)

Gross volume

I don't look at this number much because it doesn't say that much about the current state of our startup. It is a great number to look back on though. When building your startup it's easy to only focus on the MRR but it can be a nice push when looking at the gross volume. You might think: "My customers paid me this amount of money for my service." That's a nice feeling.

## Net volume from sales

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> Estimated revenue from payments after fees, refunds, disputes, and Connect transfers have been deducted.

> The above description is directly copied from Stripe. It's the text of the tooltip behind the little information icon you see below. When I use their text I prefix it with the Stripe logo.

![New volume from sales of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-02-new-volume-from-sales@2x.png)

Net volume from sales

This is very much the same as the gross volume. To me, it's equally important and I also don't use this number much. Logically, it's less than the gross volume as fees, refunds, and disputes are deducted.

## New customers

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> Number of new customers created including ones that are no longer active. Inactive customers are customers who have been deleted.

![New customers of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-03-new-customers@2x.png)

New customers

One of the things that stands out here is the spike you see in the grey line. You will see this spike in more graphs. It's because we were a target of credit card testing. [Card testing](https://www.verifi.com/in-the-news/prepared-card-testing-fraud/) happens when fraudsters test stolen credit card details by making small online purchases. The fraudsters need to check the validity of the credit card details, and once they confirm the credit card is valid they proceed with making larger fraudulent purchases. It would be great is there was a way to delete these transactions completely from Stripe, but as far as I know, this is not possible.

Back to the real number: new customers. In the last 12 months, we had 638 new customers. That's ~53 new customers per month and ~1,7 per day. You see a slight increase in customers over time. For me, this is one of the major things to work on in the next few months.

## Successful payments

Payments that didn't fail.

![Successful payments of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-04-successful-payments@2x.png)

Successful payments

For every payment, we pay a fixed fee and a percentage on top of that. For European cards, we pay 1.4% + €0.25 and for non-European cards, we pay 2.9% + €0.25. We never talked with Stripe about their fees, but we might do this once we have more payments and money flowing through Stripe.

## Spend per customer

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> Estimated revenue for all payments created with a customer, divided by the total number of customers with payments.

![Spend per customer of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-05-spend-per-customer@2x.png)

Spend per customer

One of the few numbers that don't go up within the last 12 months. This can be improved by [upselling](https://en.wikipedia.org/wiki/Upselling) to customers. As long as it's still in line with running an ethical business. I don't want to trigger people in using my product. That will not provide value for the long term and is against my values.

At the moment we offer a few things that we could limit. For example the number of websites a customer can add. Making our product paid per website would make sense. What do you think is best?

## Dispute activity & count

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> Estimated number of disputes divided by the number of successful payments in the same time series. Inquiries and Retrievals are not included in your dispute rate.

<div class="split">
  <div>
    <img
      class="border"
      src="https://assets.simpleanalytics.com/blog/github/2020-05-06-dispute-activity@2x.png"
      alt="Dispute activity of Simple Analytics from June 2019 to May 2020"
      loading="lazy"
    />
    Dispute activity
  </div>
  <div>
    <img
      class="border"
      src="https://assets.simpleanalytics.com/blog/github/2020-05-07-dispute-count@2x.png"
      alt="Dispute count of Simple Analytics from June 2019 to May 2020"
      loading="lazy"
    />
    Dispute count
  </div>
</div>

This one is new for us. We never had any disputes because we always allow customers to get a refund if they are not happy. This time a customer didn't contact us about it and arranged it with their bank. It's more costly for us and a signal we should make it more clear to our customers that canceling and getting a refund is easy.

As you can see, this is a very low number. Let's keep an eye on this though.

## High-risk payments

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> Stripe Radar uses machine learning to determine if a payment is likely to be fraudulent.

![High-risk payments of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-08-high-risk-payments@2x.png)

High-risk payments

Stripe encourages you to add their Stripe JavaScript to all your pages. So they can feed more data into their fraud AI. Simple Analytics is not a big fan of collecting too much data so we disable Stripe wherever we can. If you don't open our signup modal, we don't load the script. We want to go one step further where we don't need the Stripe JavaScript anymore. We will move it to our backend completely and make our tool completely third-party scripts free.

> See our other blog post with [practical privacy tips for your business](/practical-privacy-tips-for-your-business).

## New subscribers

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> This is the total number of new non-trial, paid subscribers (not including free plans).

![New subscribers of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-09-new-subscribers@2x.png)

New subscribers

New subscribers are something else than new customers. Subscribers are paid customers. Their trial is finished and they became a paying customer. If we look past the spike of card testing you see a slight upward trend. In the next few months, our main focus will be driving this number. We do think long term so we don't want to spend silly bucks on ads. We write good content, make deals with partners, and let our product stand out in its unique fight for privacy.

## Monthly Recurring Revenue

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> Monthly recurring revenue (MRR) is your normalized monthly revenue from all active and past-due subscriptions. It’s the best single measure of the health and trajectory of a recurring revenue business.

![Monthly Recurring Revenue (MRR) of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-10-mrr@2x.png)

Monthly Recurring Revenue

Funny enough Stripe deducts their fee from this number. Not sure why they do this, but it's not accurate at least. If you deduct their fee from our calculated MRR number it's still a bit off. This might be due to conversion rates between the dollar and the euro. Our payouts are paid in euro. If you [convert](https://api.exchangeratesapi.io/2020-05-31?base=EUR&symbols=USD) €5214 to dollars you get an MRR of \$5806 on the last day of May. We measure an MRR of \$6119 on that date. Our Stripe fees for May were \$186 which still doesn't make up for the difference of \$126 (\$5932 - \$5806). It would be great to know why there is a difference, but it's not too important to spend hours on this little number. It's a slight difference in our and Stripes calculations.

> Our MRR calculation code is open-source on our [/open page](https://simpleanalytics.com/open).

## New trials & conversion rate

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> New trials is the total number of new subscriptions that started with a free trial period. The trial conversion rate measures your success at converting trials to active subscriptions during a rolling 30-day period. Out of all trials that ended in the last 30 days, your trial conversion rate is the percentage that converted to an active subscription.

<div class="split">
  <div>
    <img
      class="border"
      src="https://assets.simpleanalytics.com/blog/github/2020-05-11-new-trials@2x.png"
      alt="New trials of Simple Analytics from June 2019 to May 2020"
      loading="lazy"
    />
    New trials
  </div>
  <div>
    <img
      class="border"
      src="https://assets.simpleanalytics.com/blog/github/2020-05-12-trial-conversion-rate@2x.png"
      alt="Trial conversion rate of Simple Analytics from June 2019 to May 2020"
      loading="lazy"
    />
    Trial conversion rate
  </div>
</div>

When we started our product was very much MVP. That also came with some underdeveloped features like automated emails about ending trial periods. We implemented this on February 4, 2020. Since then we send a reminder email 3 days before a trial ends. Also when we extend a yearly subscription we send an email 3 days before the renewal. Customers can also enable invoices for their monthly or yearly invoices.

We have some plans on improving the conversion rate. For example, when people sign up they add their website directly. Sometimes their website uses caching and we can't detect the script directly. For some people, this is a reason to cancel the trial. We can inform this in a better way and let them come back later. Maybe send them an email when their script is detected and one if we didn't detect it within one hour.

## Lifetime value

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> This is an estimate of the total revenue you can expect to collect from your average customer before they churn.

![Lifetime value of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-13-lifetime-value@2x.png)

Lifetime value

This number is expected to go up when we are around for longer. We can't have subscriptions older than our startup which is one of the reasons why we expect an increase. Some startups like [Nomad List](https://nomadlist.com/?join=nomadlist) offer a one-time-payment or lifetime deal.

![Nomad List signup modal](https://assets.simpleanalytics.com/blog/github/2020-05-nomadlist-signup.png)

[Nomad List](https://nomadlist.com/?join=nomadlist) signup modal

Because we don't know the real lifetime value yet, we will not offer this deal. It's also hard to offer a deal for all customers. A lifetime deal with a limit on page views sounds weird as well. We might offer a personal project lifetime deal but have no intention of doing so anytime soon.

## Revenue per subscriber

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> This is your average MRR per subscriber. It’s calculated by dividing your MRR by the total number of customers with an active subscription.

![Revenue per subscriber of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-14-revenue-per-subscriber@2x.png)

Revenue per subscriber

This is one of the numbers we want to actively work on. The revenue per subscriber is way too low. This is because our product has a very simple pricing model. It does not allow for the above mentioned upselling. We are working on making this more profitable for us in an ethical way.

# Retention

Retention has 3 metrics in Stripe: churn rate, churned revenue, and retention by cohort.

![Retention of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-stripe-retention.png)

Extra detailed overview of retention

## Subscriber churn rate

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> This measures the portion of your subscribers who left during a rolling 30-day period. Out of all active customers at the start of the period and any new customers in the period, your churn rate is the percentage that cancels during the period. [Stripe article](https://support.stripe.com/questions/calculating-churn-rate-in-billing).

![Subscriber churn rate of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-15-subscriber-churn-rate@2x.png)

Subscriber churn rate

Again, those spikes are not actual customers. Just ignore those. We have a churn rate of more or less 5%. This does not seem high but it's a monthly churn rate (or more accurate: 30 days). This converts to an annual churn rate of 46% (<code>1 - (1 - 0.05) ^ 12</code>). [Lincoln Murphy](https://sixteenventures.com/saas-churn-rate) wrote a great blog post on this subject.

He says having a 5% monthly churn means if you started January with 100 customers you'd have 54 customers left at the end of December. If you started with $100 in Monthly Recurring Revenue (MRR) you'd end up with $54/MRR at the end of December.

Think about it this way… over the course of the year where you start with 100 customers or $100/MRR but have a 5% monthly churn, you’d need to acquire 46 customers (or $46/MRR) just to break even with the beginning of the year. To grow by just 1 customer you'd have to acquire 47 customers! To grow by just $1, you'd have to acquire $47 in new business!

These examples are quite alarming to me. You hear many times that churn of 5% is okay, but it's not. For Simple Analytics this wasn't a big priority, but now I realize that we're just lucky with getting many new customers. If we didn't we would not be able to grow.

## Churned revenue

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> This is the total MRR lost during the period due to downgrades or cancelations (both voluntary or involuntary due to lack of payment).

![Churned revenue of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-16-churned-revenue@2x.png)

Churned revenue

I'm continuing to copy more great stuff from [Lincolns blog](https://sixteenventures.com/saas-churn-rate) about how to reduce churn. Honestly, he writes, there's nothing magical to reducing churn, it's just ensuring that your customers continue to realize value from your service.

First, though, you have to get them to start using your service – either through a sale or in a free trial – but without over-promising and by otherwise managing expectations properly. Lincoln has seen a large amount of customer churn directly correlated to missteps during the sales and onboarding phases, by the way, so keep that in mind.

I guess that we are doing quite well with managing expectations. We don't get much feedback on wrong expectations when people churn. We are them why they cancel their subscription and it's usually something that we can't do anything about.

Then, once the customer is up and running your only job is to ensure they keep realizing (more and more) value from your service.

This is something we can learn from. We don't do enough with our current customers. Let's get that setup!

## Subscriber retention by cohort

<span class="stripe-badge"><img src="https://assets.simpleanalytics.com/blog/github/2020-05-stripe-logo.svg" alt="Stripe:"></span> This table displays subscriber retention for each month following the month that the subscription started, called the cohort. If a customer unsubscribes and then resubscribes, they will be a part of two cohorts.

![Subscriber retention by cohort of Simple Analytics from June 2019 to May 2020](https://assets.simpleanalytics.com/blog/github/2020-05-17-subscriber-retention-by-cohort@2x.png)

Subscriber retention by cohort

It shows the percentages for the retention by cohort. I wonder why the total (the first row) has a retention of 72% in the 12th month but at the same time, the monthly churn rate is around 5%. Our annual churn rate should be 46%, not 28% (<code>100% - 72%</code>). Can anybody explain this?

You made it through all these numbers! Your math teacher would have been proud. If you have some experience with SaaS businesses and you can spot some easy fixes, please let me know. Happy to implement your feedback to get these numbers higher, except for churn ;)
