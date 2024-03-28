# Thorin & Co. - Testing

Visit the deployed site: [Thorin & Co.](https://thorin-legacy-8eb8ef7a277c.herokuapp.com/about/kili-and-fili)

![Thorin Responsive Site Image](static/doc/Thorin.png)

---

## Automated Testing

### HTML & CSS Validation

* [index.html](static/doc/testing/index-test.png) - Pass
* [about.html](static/doc/testing/about-test.png) - Pass
* [careers.html](static/doc/testing/careers-test.png) - Pass
* [contact.html](static/doc/testing/contact-test.png) - Pass

No custom CSS was used for this project, as the bootstrap clean blog template was used.

### JavaScript Validation

No custom JavaScript was used for this project, as the bootstrap clean blog template was used.

### Python Validation

#### Validation performed using Code Institute Pep8 Validators

* * [run.py](static/doc/testing/pep8.png) - No Errors

---

## Manual Testing

### Testing User Stories

| User Story | How is this achieved? | Evidence |
| :--- | :--- | :--- |
| I want to be able to find out more information about Thorin and his Company. | There is an about link in the navigation that will take a user to more information about the Company. The User can also click on each member to be taken to their individual page with further information about that member. | ![user story 1](static/doc/testing/us-1.png)|
| I want to be able to contact the Company. | There is a contact us link in the navigation which takes the user to a form they can fill in to contact the Company. | ![user story 2](static/doc/testing/us-2.png) |
| I want to be able to read some interesting articles relating to the Company. | The home page has a number of articles relating to the Company and the Hobbit. | ![user story 3](static/doc/testing/us-3.png) |
| I want to be able to see any job positions within the Company. | There is a careers link in the navigation. This takes the user to a careers page where any job positions will be posted. | ![user story 4](static/doc/testing/us-4.png) |

### Full Testing

| Feature | Expected Outcome | Testing Performed | Result | Pass/Fail |
| :--- | :--- | :--- | :--- | :--- |
| **Navbar** |
| Thorin & Company Logo | When clicked the user will be taken to the home page | Link clicked | Taken to the home page | Pass |
| Home Link | When clicked the user will be taken to the home page | Link clicked | Taken to the home page | Pass |
| About Link | When clicked the user will be taken to the about page | Link clicked | Taken to the about page| Pass |
| Contact Us Link | When clicked the user will be taken to the contact us page | Link clicked | Taken to the contact us page| Pass |
| Careers Link | When clicked the user will be taken to the careers page | Link clicked | Taken to the careers page | Pass |
| **Footer** |
| Twitter Icon | When clicked the user is taken to Thorin and Company's page on Twitter in a new browser window | Clicked icon | New browser window opened with Thorin and Company's twitter page | Pass |
| Facebook Icon | When clicked the user is taken to Thorin and Company's page on Facebook in a new browser window | Clicked icon | New browser window opened with Thorin and Company's facebook page | Pass |
| GitHub Icon | When clicked the user is taken to Amir Shkolnik GitHub profile in a new browser window | Clicked icon | New browser window opened with Amir Shkolnik GitHub profile | Pass |
| **Home Page** |
| Post links | Clicking on a post takes me to the site for that article in a new browser window | Clicked post link | A new browser window opened with the article | Pass |
| Older posts button | Loads older posts | clicked button | Page refreshed - This is due to there not being enough posts to check this feature works as it should, more posts would need to be added to check this works as it should | PENDING |
| **About Page**|
| Members Name | Clicking on the members name takes you to the members page with further information on them | Clicked member name | Taken to the members page with further information on them | Pass |
| **Contact Us Page**|
| Submit Button - Form not filled out | The user should be prompted to fill in the missing required fields | left form empty and clicked send | Success message displayed | ~~Fail - Added to bugs section~~ Pass - see solved bug #3 |
| Submit Button - Form filled out | A success message is displayed to the user to let them know the form has been sent, with their name inserted | Completed form and clicked send | Success message displayed with the name filled out in the name field used. *Note:* As this site was created for educational purposes to learn about using the Flask framework, the project has no backend and so the form is not sent or processed on the backend. | Pass |

---

## Bugs

### Solved Bugs

| No. | Bug | How I solved the issue |
| :--- | :--- | :--- |
| 1 | The images on the members page were not responsive and were overflowing out of their column. | Initially I had the classes featurette-img and responsive-img on the images, however it seems that these bootstrap classes are no longer used. I therefore looked at the bootstrap documentation and found the img-fluid class, which allowed me to achieve the image responsiveness. |
| 2 | Wave testing showed error that there were missing form labels| This was an easy fix, I just had to add in the for attribute on the label to connect the label to the input. |
| 3 | Form success message is being displayed even if the form is not filled in. Some fields are required so the form should be prompting users to fill in the required fields. The form currently has the required attribute on the required inputs, however some further research of the bootstrap documentation will be needed to see if there is an alternative way to achieve this as I am using bootstraps form group. | Upon looking at the form tag I discoved that there was an attribute `novalidate`. By changing this to `validate` my form now works as expected, and prompts the user to fill in any required fields in the form before submission. |

### Known Bugs

| No. | Bug |
| :--- | :--- |
