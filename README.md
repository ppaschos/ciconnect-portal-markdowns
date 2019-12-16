# ci-connect-portal-markdowns

Separate repo to keep track of editable markdown files. These markdown files
will render in the connect portal.

## Instructions to set up Webhooks:

1. Go to the settings of your repo:

![screenshot_1](/readme_images/screenshot_1.png)

2. Click on the Webhooks tab:

![screenshot_2](/readme_images/screenshot_2.png)

3. Then click on the button labeled "add a webhook":

![screenshot_3](/readme_images/screenshot_3.png)


You will be asked the following:

1. Payload URL
2. Content Type
3. Which events would you like to trigger this webhook?

For the Payload URL, just add the following url endpoint: `https://www-dev.ci-connect.net/webhooks/github`.

For the Content Type, select `application/json`

For "Which events would you like to trigger this webhook", select "Just the `push` events"

Press save and your webhook is officially set up! Updating the markdown files
in this repo will now automatically trigger the web portal to pull the latest
files from this repo and update itself accordingly. Instructions/guide to the
relevant markdown files below.


## Form Descriptions:

Files located in the `form_descriptions` directory.

These markdown files pertain to the content that appears on form input pop-overs
(on hover). For best UI/UX, each should be limited to a one sentence description if possible.

## Home Content:

Files located in the `home_content` directory.

`home_text_headline.md` will update/contain the main page's headline

`home_text_rotating.md` will update/contain the rotating text on the main page.

Each rotating text must be separated by a `/`

For example:

`Access free opportunistic cycles/ Researcher facilitation/ High throughput computing`

![screenshot_4](/readme_images/screenshot_4.png)

## Sign-up Content:

Files located in the `signup_content` directory.

`signup.md` will update/contain the headline of the sign-up page.

`signup_instructions.md` will update/contain the sign-up instructions in a listed order.

![screenshot_5](/readme_images/screenshot_5.png)

`signup_modal.md` will update/contain the acceptable use policy.

![screenshot_6](/readme_images/screenshot_6.png)

## Flash Messages:

The flash messages are set in a config file within the `flash_messages`
directory, named `flash_messages.cfg`. Each flash message route is set to a
respective message. The names of the routes must not be changed, however, the
message may be edited.

Explanation of routes within the `flash_messages.cfg` file:

`add_group_member` = Success message when adding member to project

`admin_group_member` = Success message when updating member to admin status

`approve_subgroup` = Success message when project request has been approved

`create_group` = Success message when project is created

`create_login_node` = Success message when login node is created

`create_profile` = Success message when user creates account from the portal

`create_subgroup` = Success message when sub-project is created

`delete_group` = Message when project has been successfully deleted

`deny_subgroup` = Message when project request has been successfully denied from the portal

`edit_profile` = Success message when a user's profile information/edit has been updated

`edit_subgroup` = Success message when a project's information/edit has been updated

`edit_subgroup_requests` = Success message when a project request's information/edit has been updated

`login_node_add_user` = Success message when adding user to a login node

`login_node_remove_user` = Message when user has been successfully removed from a login node

`remove_group_member` = Message when user has been successfully removed from a project

`support` = Message when user submits an email message to the osg-support staff from the portal

`view_group` = Message shown to users when they request to join a project
