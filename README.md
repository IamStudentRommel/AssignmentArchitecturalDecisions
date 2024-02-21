# Assignment Architectural Decisions

Scenario 1

You are a team responsible for developing a new mobile app for a retail company. The app will allow customers to browse and purchase products, view their order history, and track the status of their deliveries. Additionally, the app will have a loyalty program feature, where customers can earn and redeem points for discounts on future purchases. The following requirements must be considered:
1.	The retail company wants the app to support offline mode, allowing customers to browse products and view their order history even when they are not connected to the internet. The app should sync data with the server once an internet connection is available.
2.	The retail company wants to send push notifications to customers to notify them about order updates, new product arrivals, and exclusive offers. The app should integrate with a push notification service to handle the delivery of notifications.
3.	The app needs to integrate with various payment gateways to facilitate secure and convenient transactions for customers. The team should select and integrate a suitable payment gateway, or a combination of gateways based on security, ease of use, and compatibility with the app's target platforms.
4.	The retail company wants to track user behavior, such as product views, purchases, and loyalty program interactions. The team should select an analytics tool or service that provides detailed insights and metrics to help improve the app's performance and user experience.
5.	The app will display product images, which may vary in size and resolution. To ensure optimal performance, the team needs to decide on an image storage solution and implement image optimization techniques such as caching, lazy loading, and compression.
6.	The retail company plans to expand its customer base internationally. The app should support multiple languages and adapt to various cultural preferences. The team needs to implement localization techniques and decide on the appropriate localization framework or libraries.

Decision Record for a Retail Mobile App

Native, Web, or Hybrid App
The decision revolves around determining whether the application should adopt a native, web, or hybrid approach, considering factors such as performance, user experience, and development efficiency. Selecting the most suitable option is crucial, and the choice of the UI framework will significantly impact the design and implementation of the user interface.

Native App
•	Pros:  Achieves optimal performance, ensures fluid user experience, and leverages platform-specific features for enhanced functionality.
•	Cons: Requires separate development efforts for iOS and Android, potentially resulting in extended project timelines.

Web App:
•	Pros: Provides compatibility across various platforms, allows for efficient updates, and can be accessed through standard web browsers.
•	Cons: Faces limitations in accessing device-specific features and may experience performance trade-offs.

Hybrid App:
•	Pros: Balance between cross-platform compatibility and native-like experience, single codebase.
•	Cons: May not consistently match the performance of native apps in certain scenarios.

Decision:
The development will focus on creating a mobile app with native features.

Justification:
A native mobile app is preferred in this scenario due to its superior speed and responsiveness, despite the potential need for separate codebases. In retail applications, where performance is crucial for seamless user interactions and real-time updates, the optimized and platform-specific nature of native development ensures an enhanced user experience, making it the preferred choice over alternatives like web or hybrid apps.
UI Framework
Choosing the UI framework for the application will focus on meeting key features crucial for the retail company's needs. This decision is based on the company's detailed identification of essential features vital for the mobile app's success.

Offline Mode Support:
•	Rationale: Enable customers to browse products and view order history offline, with data synchronization once an internet connection is available.
•	Recommendation: The selected UI framework should seamlessly facilitate offline mode capabilities and efficient data synchronization.

Push Notification Integration:
•	Rationale: Integrate with a push notification service to notify customers about order updates, new product arrivals, and exclusive offers.
•	Recommendation: The UI framework must support easy integration with push notification services for effective communication with users.

Payment Gateway Integration:
•	Rationale: Integrate with various payment gateways for secure and convenient transactions.
•	Recommendation: The chosen UI framework should allow seamless integration with selected payment gateways, considering factors such as security, ease of use, and platform compatibility.

Analytics Integration:
•	Rationale: Integrate with an analytics tool or service to track user behavior and gather insights.
•	Recommendation: The UI framework must support integration with analytics services that provide detailed metrics to enhance app performance and user experience.

Image Handling and Optimization:
•	Rationale: Display product images of varying sizes and resolutions with optimal performance.
•	Recommendation: The UI framework should accommodate an image storage solution and support image optimization techniques, including caching, lazy loading, and compression.

Internationalization and Localization:
•	Rationale: Support multiple languages and adapt to cultural preferences for international expansion.
•	Recommendation: The UI framework must enable the implementation of localization techniques, with a focus on selecting appropriate localization frameworks or libraries.

Decision:
The User Interface will be built using the React Native framework.

Justification:
React Native is the most appropriate one for the UI framework in the retail app due to the following reasons.

•	Enabling the development of cross-platform applications with a single codebase, React Native promotes efficient resource utilization and expedites development timelines. This aligns with the retail company's objective of delivering a consistent user experience across diverse platforms.
•	With a rich collection of pre-built components and a declarative syntax, React Native facilitates the creation of visually appealing and responsive user interfaces, enhancing the overall design quality.
•	Ensures smooth integration with native modules.

In addition to this, to ensure a smooth and visually pleasing design experience for users, the team will utilize Native Wind. Constructed on top of Tailwind CSS for React Native, this framework can effectively develop contemporary and responsive mobile applications by integrating the capabilities of Native Wind with React Native. The utility-first approach of Native Wind allows straightforward customization of UI components, ensuring a robust foundation for constructing visually appealing and high-performing cross-platform mobile applications.


Backend Language
Choosing the appropriate backend language is vital as it directly impacts the retail application's performance, responsiveness, and its ability to adapt to the dynamic requirements of a retail environment.

Decision:
The backend development will utilize Node.js.

Justification:
Node.js, with its lightweight nature and extensive ecosystem of packages, aligns well with the project's requirements, making it a suitable choice for a backend that needs to handle concurrent requests efficiently. Its proficiency in handling asynchronous operations further enhances its appropriateness for the task.

Permissions
As the application endeavors to offer advanced features such as offline mode, push notifications, secure payment gateways, user behavior tracking, image optimization, and internationalization. To implement these functions, the team needs to establish a strong permissions model that regulates access and interactions within the application.

Decision:
The application will utilize JSON Web Tokens (JWT) to handle authentication and implement role-based access control (RBAC) for authorization.

Justification:
Utilizing JSON Web Tokens (JWT) for authentication and Role-Based Access Control (RBAC) for authorization is the best choice. JWT ensures secure user authentication with digitally signed tokens, promoting scalability and reducing server-side storage needs. Combined with RBAC, which assigns roles to users, this model provides a flexible and detailed permissions structure.

Data Storage
The criteria for selecting the data storage approach in the retail mobile app prioritize ensuring a seamless and responsive user experience while striking a balance between offline functionality and data synchronization. The chosen approach should be widely used, dependable, and high performing. It should also seamlessly manage structured data and integrate effectively with various technologies.

Decision:
The data will be stored in a relational database, specifically using MySQL.

Justification:
MySQL is a dependable and widely used choice for storing data. It efficiently manages structured data in relational databases, providing quick and responsive data retrieval. Its open-source nature makes it cost-effective and accessible for various applications.

Additional frameworks or technology stacks
The retail app should consider leveraging technologies known for their fast data synchronization capabilities to enhance the overall user experience. Utilizing such technologies is crucial as it ensures a seamless, real-time, and dependable experience for users. Fast data synchronization guarantees that users can access the most up-to-date and pertinent information, fostering a positive user experience and elevating customer satisfaction.

Decision:
Firebase integration will be deployed to achieve real-time synchronization of data.

Justification:
Firebase integration in a retail app is vital for real-time updates, ensuring users receive the latest information instantly. It enhances the user experience, providing quick access to product details. Firebase also offers a reliable backend, ensuring app performance and scalability. With added security features and functionalities like cloud storage and push notifications, Firebase has become an asset, contributing to an improved and responsive retail app.

