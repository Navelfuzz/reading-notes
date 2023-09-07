# CF 401: Java // Reading Notes

## Class 42: Ad ad ad ad ad ad ad mob

## Readings

[Google AdMob (we’re using this to display ads)](https://developers.google.com/admob)

### Questions

1. How are the ads shown in your application determined when using Google AdMob?
2. Whate are the platforms which support Google AdMob?

### Answers

1. `How Ads Are Shown in Your Application with Google AdMob`:
Google AdMob uses a combination of factors and algorithms to determine which ads to show in your mobile application. Here's a simplified overview:
* Ad Request: When a user interacts with your app (e.g., opens a screen or navigates within the app), your app sends an ad request to Google's AdMob servers.
* Ad Inventory: Google AdMob maintains a large inventory of ads from advertisers who want to reach specific audiences or demographics.
* Targeting and Contextual Information: AdMob considers various factors to determine which ad is the most relevant and likely to perform well in your app. This includes factors like the user's location, device type, demographics, user interests, and contextual information about the app's content.
* Real-Time Bidding (RTB): AdMob often uses real-time bidding, where advertisers bid in real-time to have their ads displayed to a specific user. The highest bidder's ad is selected to be displayed to the user.
* Ad Formats: AdMob supports various ad formats, including banner ads, interstitial ads, native ads, and rewarded ads. The chosen ad format depends on the available ad space in your app and the user's behavior.
* User Experience: AdMob aims to provide a positive user experience, so it may prioritize showing ads that are less intrusive and relevant to the user's interests to prevent excessive ad interruptions.
* Auction and CPM: AdMob uses an auction system where advertisers compete for ad space. The ad that provides the highest CPM (Cost Per Mille, or cost per thousand impressions) often wins the auction and gets displayed.
* Ad Load Frequency: AdMob allows you to set limits on how often ads are shown to users to prevent ad fatigue and maintain a good user experience.

In summary, AdMob uses a combination of user data, ad inventory, bidding, and contextual information to determine which ads to show to users. The goal is to maximize revenue for the app developer while providing relevant and engaging ads to users.

2. `Platforms Supported by Google AdMob`:
Google AdMob is primarily designed for mobile app monetization and supports various mobile platforms, including:
* Android: AdMob fully supports Android applications, allowing developers to integrate ads into Android apps published on the Google Play Store and other Android app distribution platforms.
* iOS: AdMob also provides robust support for iOS applications, enabling developers to monetize their apps on iPhones, iPads, and other iOS devices through the Apple App Store.
* Unity: AdMob offers a Unity plugin for game developers, allowing them to integrate ads into games created with the Unity game engine. This extends AdMob support to cross-platform games.
* Cocos2d-x: AdMob provides a plugin for the Cocos2d-x game development framework, making it compatible with apps developed using this popular platform.
* Flutter: Google AdMob has a Flutter plugin, making it accessible to developers creating apps using the Flutter framework for cross-platform mobile app development.

In addition to these platforms, AdMob also supports various ad formats, including banner ads, interstitial ads, native ads, and rewarded ads, providing flexibility for app developers to choose the ad types that best fit their apps and user experiences.

[Google's monetization guide](https://play.google.com/console/about/guides/monetize/)

### Questions

1. What are some of the ways you can make money in your app by monetizing with Google?

### Answers

1. Money Moves: 

* In-App Advertising (AdMob): Integrating Google AdMob into your app allows you to display ads to users. You earn revenue based on ad impressions (CPM), ad clicks (CPC), or other engagement metrics. There are various ad formats to choose from, including banner ads, interstitial ads, native ads, and rewarded ads. AdMob provides targeted ads that are relevant to your users, enhancing the potential for higher earnings.
* In-App Purchases: You can offer virtual goods, premium features, or digital content for purchase within your app. Google Play Billing makes it easy to set up and process in-app purchases. This monetization method is often used in freemium apps, where the app is free to download, but users can make purchases to enhance their experience.
* Subscription Models: Implement subscription-based pricing models, where users pay a recurring fee (e.g., monthly or annually) to access premium content or features. This approach is common in news apps, streaming services, and productivity apps.
* Affiliate Marketing: Promote products or services related to your app's niche and earn commissions for each sale or action generated through affiliate links or codes. Google's affiliate network, such as AdSense for Content, can help you find relevant affiliate partners.
* Sponsored Content: Partner with advertisers or brands to feature sponsored content within your app. This could include sponsored articles, videos, or interactive content that aligns with your app's audience and provides a revenue share for your app.
* Selling Merchandise: If your app has a strong brand or community, consider selling merchandise related to your app's theme. This could include clothing, accessories, or physical products that resonate with your user base.
* Data Monetization: Collect and anonymize user data (while respecting privacy regulations) and offer insights or market research reports to interested parties or businesses. This method is more common in data-centric apps.
* Donations and Crowdfunding: Some apps rely on user donations or crowdfunding platforms to generate revenue. Users who appreciate your app's value may choose to contribute financially to support its development and maintenance.
* Licensing and White-Labeling: If your app offers unique functionality or technology, you can license it to other developers or businesses for use in their projects. White-labeling involves offering your app under a different brand or label to other businesses.
* Cross-Promotion: Promote other apps or products within your app in exchange for revenue-sharing agreements with developers or businesses. This method can be beneficial for apps with a substantial user base.
* Event and Ticket Sales: If your app is related to events, conferences, or entertainment, you can sell event tickets or offer a platform for event organizers to promote and sell tickets, earning a commission on each sale.
* Consulting and Services: Use your app as a lead generation tool for consulting, services, or professional expertise related to your app's niche. Offer premium services to users or businesses in need of specialized assistance.
