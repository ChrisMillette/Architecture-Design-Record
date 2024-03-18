# Architecture-Design-Record

# Scenario 1 Architecture Decision Record
Christopher Millette

# Decision 1: Native, web, or hybrid app
## Context
-	Mobile application that must support offline mode, notifications, multiple languages, and transaction services. The application will also have to make use of the device’s hardware.
## Decisions
-	Native mobile app for both IOS and Android OS. This will allow development to optimize performance on devices that support each platform and take advantage of their individual capabilities. This will also allow for a better user experience, allowing the application to follow each platform’s design conventions.
## Consequences
-	Better performance with native development.
-	Separate code for each platform will create a higher workload.

# Decision 2: UI Framework
## Context
-	UI Framework must be both visually appealing and conform to platform design guidelines.
## Decisions
-	SwiftUI for the IOS platform and Jetpack Compose for Android Platforms. Both frameworks are developed by the same company that develops the platforms, making it easier to conform to each platform’s design guidelines. Each framework also comes with design tools that will decrease development time, declarative syntax, and performance optimization for their native platform.
## Consequences
-	Platform specific frameworks will create differences in the application on each platform.
-	SwiftUI and Jetpack Compose may require additional training.
-	Jetpack Compose supports Android 5.0 and later, older phones will not be compatible.

# Decision 3: Backend Language
## Context
-	A backend language must be chosen to develop the server-side components including notification delivery, data synchronization, and payment management.
## Decisions
-	Node.js will be used for backend development. Node.js offers scalability, a large collection of libraries and frameworks, allows for rapid deployment, and its event driven architecture is perfect for handling requests simultaneously.
## Consequences
-	Node.js does not work well with relational databases, will require additional libraries and frameworks.
-	Node.js will reduce the development time of components.

# Decision 4: Permissions
## Context
-	The application will require certain permissions from the user to enable requested features like offline functionality, notifications, and accessing device hardware.
## Decisions
-	Permissions will be requested at runtime and provide clear explanations for the need of each one for transparency. The application will require camera permission, permission for push notifications, and storage permission to enable offline use.
## Consequences
-	Excessive requests may lead to user distrust.

# Decision 5: Data Storage
## Context
-	The application will need to store product information, order history, user settings, and various other types of data and synchronize server side data with client side to allow offline use.
## Decisions
-	SQLite will be used for data storage. This will allow for caching, lazy loading, and compression, as well as data synchronization to keep local data up to date for offline use.
## Consequences
-	SQLite will enable the application to store a local cache of data.
-	Regular performance evaluations will be needed as data grows over time.


# Decision 6: Localization
## Context
-	The application will need to support multiple languages for future customer base expansion.
## Decisions
-	The i18next framework will be used to easily localize any UI elements in combination with conventional localization. This library will also help manage translations and make sure the application stays consistent across different languages. 
## Consequences
-	Reduced localization workload. 
-	Continuous testing will be required to ensure the accuracy of translations.

# Decision 7: Analytics
## Context
-	The application will have to track user interactions and app performance.
## Decisions
-	Google Analytics will be used for analytics, this will also give access to Google’s unique insights that it collects from it’s own userbase in combination with the data collected from the application. This will ensure that analytics are accurate, and interpretation can be partially automated with machine learning.
## Consequences
-	Analytics reports will have to be evaluated on a regular basis to make sure relevant event tracking is in place.

