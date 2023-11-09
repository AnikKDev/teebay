## Areas for Improvement

### Frontend

There are always areas that can be enhanced. Potential improvements include:

- **State Management Enhancements:** Implementing more sophisticated state management solutions like Apollo Client's reactive variables or integrating Redux for complex application states. Right now there is no state management libray have been used. Only context api has been used for it. Possible improvements can be react's state management hooks, redux or zustang.
- **Performance Optimization:** Further optimizing the application to reduce load times, such as implementing lazy loading for images and dynamically imported components.
- **Type Improvements:** To enhanace the dev environment many type declaration from typescript can be improved. Right now even though this project is using typescript for development, but there are always scope for improvement in this. Although it won't affect it in client side as TS doesn't run in client side.
- **Testing Suite Expansion:** Currently, the application doesn't have any testing suite. Expanding this to include more end-to-end tests and integration tests would increase reliability.
- **User Experience (UX) Enhancements:** Continuous user feedback is essential. Based on user testing, the UX can be further refined and improved. Added products can be edited into fullest. Right now edit product is not properly implemented. Delete too.
- **DRY:** There are some cases where had to use repeatative code. It can be reduced.
- **Generic Error:** I have used mantine ui's useForm for validationg the forms. But upon database actions, the system doesn't show a proper error message. It can be improved.
- **Docker compose:** Docker compose is not migrating the prisma. hence running docker compose, we can't perform actions with database yet. to make it work, we might need to do some configuration in prisma config file to run the migration before doing everything. so that the database tables are created beforehand doing any actions from frontend or backend.

### Backend

There are always areas that can be enhanced. Potential improvements include:

- **Proper Error response:** Even though the error that sents by graphql can be readable by devs but sometimes it seems pretty hard to understand by the end user. So A proper error handling module can be made that will handle different cases for errors and return a proper readable error.
- **DB Design:** Database modeling and relations can be improved by adding some more relations and tables. Such as, categories for products can have a separated table `categories`. And it can be a many-to-many relation like, a product can belogs to multiple categories. and in each category there can be multiple products.
- **Security Enhancements:** We could use token based auth system to level up the api security. and a refresh token can be generated to for the default token. with it we can evaluate the user permission.
- **Role based routing:** There can be multiple roles. Seller, buyer, admin and super admin, each role indeed is a User role. so based on the role, we can reduce or increase the actions that a user can perform.
- **DRY:** There were some cases where I had to use repeatative code. Although I tried to reduce it in this limited time, but it is not perfect. Hence we could use some util funtions or methods that will take some parameters and in return it will return the result that way we can use this function or method in places where we need it. This can be a solution to reduce the repeatativeness of code.
- **Test Cases:** I haven't written any test cases or github actions here. although I had a template ready for REST api based backend. there I had husky to check precommit actions. THat was for linting only. But we could improve it by adding more edge cases here and we can niclude github actions too.
- **Docker compose:** Docker compose is not migrating the prisma. hence running docker compose, we can't perform actions with database yet. to make it work, we might need to do some configuration in prisma config file to run the migration before doing everything. so that the database tables are created beforehand doing any actions from frontend or backend.

Above I have tried to metion some code level improvement that I can think of to make this product atlease an MVP.

### Extra improvements

- **Git branching:** we can maintain a proper git branching strategy too for particular feature, or fixes or even hotfixes. It can help use to rollback through changes each branch has.
- **Separate UI:** We can have separate ui's for buyers, sellers and admin. Also we can have dashboard for each of the UI. Either we can do this in this single domain or we can create subdomains for each role.
- **UI:** The ui design can be improved too. To make user experience good enough, we must need a user friendly and aesthetic ui design. Obviously it will be depended on what client requires.
- **Bigger Picture:** While developing we shouldn't think of 1 or 100 users. We have to think of thousands of users. If thousands of users uses our application simultanously what would we do?...how our system will perform?...like this. So based on that perspective there is always scope to improve in code, system and operation level.
