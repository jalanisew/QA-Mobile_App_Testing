E-Commerce Demo App – Manual Testing Project

--Project Overview--
This repository documents the manual testing performed on the **E-Commerce Demo Android application (v3.2.0)**.
The testing focused on validating the app’s core user flows, UI behavior, API responses, and app stability under various conditions.


--Testing Scope--
* Functional Testing
* UI & Responsiveness Testing
* Interrupt Testing
* Permissions Testing
* API Validation using Postman
* Documentation & Defect Tracking (Excel + GitHub + Jira)


--Platforms Tested--
* Samsung Galaxy M21 – Android 13
* Pixel Emulator – Android 14


--Test Coverage Summary--
* Total Scenarios Covered: 25
* Test Cases Designed: 25
* Modules Tested:
  * Installation & App Launch
  * Login & Profile
  * Product Catalog
  * Cart & Checkout
  * Notifications
  * Permissions
  * UI & Accessibility
  * Interrupt Handling


--Execution Results--
* Total Test Cases: 25
* Passed: 16
* Failed: 9


--Defect Severity Breakdown--
Severity | Count 
Critical | 2     
Major    | 4     
Minor    | 3     


--Key Defects Identified--
* Checkout allowed even when the cart was empty.
* Cart quantity update did not reflect in the database.
* Notification deeplink opened incorrect screens.
* Profile and login input fields lacked proper validation.
* UI alignment issues on smaller screens.


--API Validation Summary--
* Login API: Returned expected responses for both valid and invalid credentials.
* Catalog API: Product list matched UI results.
* Cart API: Add-to-cart worked, but quantity update failed (linked to BUG-03).
* Checkout API: Returned success even with an empty cart (BUG-04).
* Notifications API: Returned data but deeplink was inconsistent (BUG-05).


--Risks & Limitations--
* Testing performed only on Android, no iOS coverage.
* Demo app lacks real payment gateways.
* Backend database was not accessible; SQL validations were done using example queries only.
* Push notifications were simulated, not triggered by a live server.


--Recommendations--
* Fix cart logic and enforce proper checkout validation.
* Improve validation for login and profile fields.
* Enhance UI responsiveness and accessibility scaling.
* Ensure consistency in notification deeplinks.
* Conduct full regression testing after fixes are implemented.


--Conclusion--
The E-Commerce Demo Android application was tested across functional, UI, interrupt, and API perspectives.
Out of 25 test cases, 16 passed and 9 failed, uncovering 9 defects (critical, major, and minor).
While the core flows are operational for demo purposes, key improvements are required in cart behavior, checkout validation, and notification handling.

