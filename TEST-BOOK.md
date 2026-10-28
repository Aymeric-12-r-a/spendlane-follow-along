# Spendlane test book

Preconditions for the calculator: the home page is open. Preconditions for the demo form: `/demo` is open. Expected results are computed by hand from the stories.

| Id | Story | Input | Expected result |
| --- | --- | --- | --- |
| TC-01 | Calculator | 50 employees, 4 reports | 33.3 hours saved per month |
| TC-02 | Calculator | 1 employee, 1 report | 0.2 hours saved per month |
| TC-03 | Calculator | 5000 employees, 30 reports | 25000 hours saved per month |
| TC-04 | Calculator | Employees empty, 4 reports | "Enter 1 to 5000 employees and 1 to 30 reports per employee." |
| TC-05 | Calculator | 0 employees, 4 reports | Same message |
| TC-06 | Calculator | 5001 employees, 4 reports | Same message |
| TC-07 | Calculator | 50 employees, 31 reports | Same message |
| TC-08 | Demo form | Karim Haddad, karim@northwind.io, 11 to 50 employees | "Thank you" and "Our team will contact you within one business day." |
| TC-09 | Demo form | Karim Haddad, karim@, 11 to 50 employees | "Enter a valid work email." next to the email |
| TC-10 | Demo form | Empty name, karim@northwind.io, 11 to 50 employees | "Enter your full name." next to the name |
| TC-11 | Demo form | Karim Haddad, karim@northwind.io, no company size | "Choose your company size." next to the field, no thank-you message |
| TC-12 | On a phone | Home page and `/demo` at 375 pixels wide | No sideways scrolling; every field and button reachable |
| TC-13 | Calculator | 50 employees, 0 reports | "Enter 1 to 5000 employees and 1 to 30 reports per employee." |

## Campaign on version 1.0

> Version 1.0, production, laptop and 375 pixels. 13 cases run: 12 passed, 1 failed (TC-11, the demo form accepts an empty company size). One question from exploration: should the full name have a maximum length?

| Id | Obtained result | Status |
| --- | --- | --- |
| TC-01 | 33.3 hours saved per month | Pass |
| TC-02 | 0.2 hours saved per month | Pass |
| TC-03 | 25000 hours saved per month | Pass |
| TC-04 to TC-07 | "Enter 1 to 5000 employees and 1 to 30 reports per employee." | Pass |
| TC-08 | "Thank you" and "Our team will contact you within one business day." | Pass |
| TC-09 | "Enter a valid work email." next to the email | Pass |
| TC-10 | "Enter your full name." next to the name | Pass |
| TC-11 | "Thank you" page, no error next to the company size | Fail |
| TC-12 | The home page and `/demo` are 375 pixels wide, nothing scrolls sideways | Pass |
| TC-13 | "Enter 1 to 5000 employees and 1 to 30 reports per employee." | Pass |
