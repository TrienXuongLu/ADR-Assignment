# ADR: Retail Management

## Date
2023-10-10

## Context

### Status
Proposed

### In the Context of Use Case
Our development team has taken on the task of creating a high-speed, reliable, secure, and maintainable mobile application for a retail company client. Our application will be used by consumers (customers) and will include delivery tracking, facilitating web browsing, purchasing, order history retrieval, and will include a customer loyalty program where users can earn and redeem site points to be used as a discount on future purchases.

### Facing
Our client requires us to implement an offline mode feature where users can have full non-interrupted access to product browsing and load their order history without the need for internet connectivity. Our application must also focus on having secure payment options that are fully reliable, available and convenient for the user to use multiple different payment options on the application. Our application needs to include a responsive and fast push notification feature that updates the user on their order status, new products, and exclusive offers. Our app would need to ask the user for permission to use analytic tools for application improvement and to show ads or products that the user would be interested in. Being a retail application, we need to efficiently render images of all sizes and multiple images per product and have support for multiple languages to include an international customer base.

### We Decided For
•	Application Type: Native Application for iOS and Android. Being native this would utilize the full potential of each operating system, being fast and responsive would provide users with the quality that would be expected in an application.
•	UI Framework: React Native, we chose this for the availability of support, and having the ability to reuse code across different platforms, which would open the ability for maintenance/upgrades and speed up the development process for our team. With React Native being open source, it is constantly being improved and has a great user interface that is built to provide developers with an easy to navigate workspace.
•	Backend Language: Node.js was chosen for this application for its efficiency and delivers a good native user experience to follow our theme of delivering and utilizing native like tools for development. One of the biggest influences in our group choosing Node.js was for its non-blocking I/O operations. This allows our program to maintain its efficiency and speed while giving the client a smooth experience while making requests.
•	Permissions: Our application will make sure the user has given permission to collect necessary data only and will safeguard all private user information and privacy and be in check with the platform/application guidelines.
•	Data Storage:
o	Local: SQLite will be used for this application for its offline data access and storage, which will help our application store information reliably and allow the offline access that is requested by our client. Having a well-known and highly spoken of storage service is key to our application.
o	Remote: Amazon S3 will be used for its reliability and support that is available, and has scalable image storage, which is important for expansions and upgrades to the application. MongoDB will be used for high-performance transactional data storage.
•	Other Frameworks/Stacks:
o	Payment: Our app will be implementing Stripe, for its popularity and security that has been shown throughout its years, providing user-friendly and convenient payment processing. We will also include PayPal as a payment option for the trust factor as well as its availability in more than 200 countries, allowing users from around the world to have a payment option other than what Stripe supports.
o	Push Notification Service: We will be utilizing Firebase due to its reliability and integration for iOS and Android which can be potentially added to a web application for use in the future. With its priority notification features as well as location and time zone-based notifications, it suits our program well to be used world-wide.
o	Analytics/Support: Our app will use Google Analytics for its safe and secure tracking and performance when applied to users and has various techniques and options for image optimizing including caching, compression, and loading. We will also be utilizing React Natives localization packages to support the multi-language request our client requested. The i18n library will also be implemented for translation purposes and was an easy decision with its lightweight load and compatibility with almost any framework to help support customers and create an easy experience for international users.

### To Achieve
•	Smooth, reliable, and fast image loading and rendering
•	Well informed and useful push notifications that are delivered instantly
•	A smart and secure user analytics service that improves user experience and the application
•	An efficient experience for users in both online and offline browsing
•	High quality language and caption implementations to support a worldwide market
•	A reliable, secure, and widely trusted payment system for quick transactions with the user

### Accepting Downside
•	Choosing to develop a Native Application for both iOS and Android will require a lot of resources and time management with developers working to optimize the service on each operating system adapt to each platform’s requirements and test each operating system rigorously.
•	While our team attempted to use frameworks and technologies that have been shown to work well together and integrate easily, there will still have to be a lot of navigating and adapting to ensure each component works as designed. This will require tons of work to ensure perfect integration and constant testing of each component in every way possible to ensure the application is working as intended.

## Discussion
Since the mobile application is dominating every industry to bring users a brand-new technology era where users only need mobile phones to perform their daily tasks, such as grocery shopping, bill payments, appointment bookings, etc. Not only the retail industry but also other industries are trying to increase revenue by applying this mobile technology trend. Whereas organizations invest a huge amount of money into this mobile technology field to bring customers the most convenient app that users ever have, a company will fall behind if it couldn’t catch up with the mobile technology trend.
To make the app stand out among giant retailers’ applications, we will design the application which allows users to access without internet access. Every action, such as adding a product to the cart, product payment, browse product, etc., will be automatically synced to our database centre as soon as users’ mobile phones connect to the internet. To help the retail company generate more sales, we maximize some features, such as new product roll-out, exclusive promotions for a target user, etc., in order to offer the most effective promotion, we use users’ history of product purchases, browsing history, and product added into cart. Besides, we also use Google Analytics to understand our customers’ behaviours and habits; by doing that we can design sale funnels or purchasing journeys which lead users to the payment stage smoothly. Additionally, we can add upselling or cross-selling in each sale funnel which recommends users a complete package with a product they are purchasing.
As we are also aware that we somehow track users’ behaviour quite a bit, users will question their privacy and security issues while using the app. We will design our application to allow users to activate and deactivate permission to allow us to perform such an activity. Beyond that, we integrate the application with the Stripe payment system which is well-known for security and user-friendliness; with this feature in our application, users will have peace of mind while using the application. As we are expanding the application to an international level, we add an extra payment option, PayPal; consumers will have more options to make payments.

## Decision
Here are solutions that we decide to integrate into the application:
•	Application Access
o	We apply SQLite, Amazon S3 and MongoDB for Data Storage to maximize user experience. Whether users access the application with or without internet access, users will have no trouble using the application, and all functions and features of the application will function the same.
•	Payment
o	We will partner with Stripe to bring peace of mind to customers of its’ popularity and high-rated user experience. We also include PayPal as another payment option because it is being used in over 200 countries; customers will have more choices to make payments.
•	Order Tracking
o	As online shopping is one of the main sources of retailers’ revenue, we will integrate our application with a 3PL (Third-party Logistics) to allow users can track their order deliveries as well as more delivery options.
•	Notification
o	With the advanced technology continues growing, manufacturers take advantage of the growth of technology to innovate and invent much more convenient products to bring their users the most restful life. We design the application with effective promotions which notify users of a new product roll-out, offer a sale funnel, and encourage outstanding promotion.
•	Analytic Tools
o	Besides asking users to allow the retail company to track their behaviours and history of products, we also use Google Analytics to design the application which brings convenience and familiarity and offers more effective marketing advertising.
•	Programming Language
o	We decided to use React Native and Node.js to make the application. This programming is known for its popularity, performance and usability.

## Consequences
•	Offline Mode Implementation
o	By supporting offline browsing and order history access, the app ensures continuous user engagement even without internet connectivity. However, this might increase the app's complexity, requiring more robust synchronization mechanisms when the device goes online.
•	Multiple Payment Options
o	Integrating multiple payment gateways ensures flexibility and convenience for users. This decision, though beneficial for user experience, demands rigorous security measures and continuous monitoring to ensure transaction safety.
•	Push Notifications
o	The responsive push notification system enhances user engagement, informing them about order statuses and exclusive offers. On the other hand, too frequent notifications might be perceived as intrusive, requiring a balance in frequency and relevance.
•	Permissions for Analytics and Ads
o	While analytics can provide valuable insights for app improvement, seeking permissions might be a hurdle in user onboarding. Proper transparency about data usage is crucial to maintain trust.
•	Multi-language Support
o	Catering to an international audience by providing multi-language support broadens the app's market reach. However, it entails continuous updates and maintenance for each language version, especially during feature releases or content updates.
•	Native Application Development
o	Opting for a native application ensures optimized performance and responsiveness for each OS. Yet, it might slightly increase development efforts since platform-specific nuances have to be addressed.
•	Using React Native
o	The choice of React Native as the UI framework facilitates code reusability across platforms, speeding up development. Nevertheless, any platform-specific customizations or integrations might demand additional efforts.

These consequences, both positive and potentially challenging, guide our ongoing design, development, and maintenance strategies, ensuring the app remains user-centric, secure, and technologically sound.