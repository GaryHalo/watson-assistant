---

copyright:
  years: 2015, 2022
lastupdated: "2022-11-03"

keywords: Watson Assistant release notes

subcollection: watson-assistant

content-type: release-note

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:external: target="_blank" .external}
{:deprecated: .deprecated}
{:important: .important}
{:note: .note}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}
{:video: .video}

{{site.data.content.classiclink}}

# Release notes for Watson Assistant
{: #watson-assistant-release-notes}

Find out what's new in {{site.data.keyword.conversationfull}}.
{: shortdesc}

This topic describes the new features, changes, and bug fixes in each release of the product. For more information about changes in the web chat integration, see the [Web chat release notes](/docs/watson-assistant?topic=watson-assistant-release-notes-chat).

## 3 November 2022
{: #watson-assistant-nov032022}
{: release-note}

Never ask a step
:   There may be some situations where you need a step to never ask a question because you anticipate there might be redundant questions in the conversation. A new setting, **Never ask**, is now available for any step that expects a customer response. For more information, see [Skipping steps, always asking steps, or never asking steps](/docs/watson-assistant?topic=watson-assistant-collect-info#collect-info-skip-step).

Action notes
:   You can now add free-form notes to each action. Within each action, you can use **Action notes** to add a description, documentation, comments, or any other annotations to help you keep track of your work as you build an action. For more information, see [Using the action editor](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-build-actions-overview#build-actions-overview-use).

Variable values in Preview
:  Viewing action variables in Preview has been improved. Now you can see the history of all action variables, rather than one action at a time. For more information, see [Variable values](/docs/watson-assistant?topic=watson-assistant-review#review-variable-values).

## 21 October 2022
{: #watson-assistant-oct212022}
{: release-note}

Algorithm version updates
:   The algorithm version setting for both actions and dialog now includes three choices: beta, latest, and previous. For more information, see [Algorithm version](/docs/watson-assistant?topic=watson-assistant-algorithm-version).

## 12 October 2022
{: #watson-assistant-oct122022}
{: release-note}

`now(String timezone)` method output includes time zone offset
:   The string returned from the `now(String timezone)` method now includes the time zone offset (such as `-05:00`). The new format is `yyyy-MM-dd HH:mm:ss 'GMT'XXX` (where `XXX` represents the time zone offset). This change enables accurate time zone computations when used with other date and time methods such as `before`, `after`, and `reformatDateTime`.

    If you have an existing action or dialog that depends on the previous format, you can adapt it by reformatting the output using `now(timezone).reformatDateTime('yyyy-MM-dd HH:mm:ss')`.
    
    For more information, see [Expression language methods for actions](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-expression-methods-actions#expression-methods-actions-now).

## 23 September 2022
{: #watson-assistant-sep232022}
{: release-note}

Upload an image as a preview background
:   On the **Preview** page, you can now upload an image of your organization's website as a background. For more information, see [Previewing and sharing your assistant](/docs/watson-assistant?topic=watson-assistant-preview-share).

## 16 September 2022
{: #watson-assistant-sep162022}
{: release-note}

Session ID information on Analyze page
:   Session ID information for conversations is now displayed on the Conversations tab of the Analyze page. You can also filter customer conversation data by the session ID. From the Conversations tab of the Analyze page, use the Keyword filter to search by session ID. For more information, see [Filtering conversations](/docs/watson-assistant?topic=watson-assistant-analytics-conversations#analytics-conversations-filtering).

   The ability to filter on session ID has limited support for conversations that occurred before this feature release. For all conversations that occurred before 16 September 2022, you can filter only by a single session ID at a time.

## 9 September 2022
{: #watson-assistant-sep092022}
{: release-note}

New operators available for building conditions
:   Several new operators are available for building conditions in your actions. The options response type now has the `is any of` and `is none of` operators available. For more information, see [Operators](/docs/watson-assistant?topic=watson-assistant-step-conditions#operators).

Copy actions to other assistants
:   You can copy an action from one assistant to another. When you copy an action, references to other actions, variables, and saved responses are also copied. For more information, see [Managing actions](/docs/watson-assistant?topic=watson-assistant-manage-actions).

Filter variables and saved responses by name
:   You can now find variables and saved responses more easily. On the Actions page, you can filter variables you created or saved responses you added. Click the search icon, then enter a search string. Your list of variable or saved responses filters to match what you enter.

## 1 September 2022
{: #watson-assistant-sep012022}
{: release-note}

Conditioning on days of the week
:   You can now condition a step on days of the week. This feature is available with the _date_ response type and the _Current date_ built-in variable.

    For example, you might [define a customer response](/docs/watson-assistant?topic=watson-assistant-collect-info#choose-type) in step 1 with the date response type. When the customer responds to that step, they choose a date. You can then condition a later step on whether the date that the customer chose is Wednesday.

New operators available for building conditions
:   Several new operators are available for building conditions in your actions. The free text response type now has the `contains`, `does not contain`, `matches`, and `does not match` operators available. For more information, see [Operators](/docs/watson-assistant?topic=watson-assistant-step-conditions#operators).

Extensions support for arrays
:   Custom extensions now support passing arrays as parameters and accessing arrays in response variables. For more information, see [Calling a custom extension](/docs/watson-assistant?topic=watson-assistant-call-extension).

## 26 August 2022
{: #watson-assistant-aug262022}
{: release-note}

New filter on the Analyze page
:   You can now filter customer conversation data by the _Greet customer_ system action. From the Conversations tab of the Analyze page, open the Actions filter and select **Greet customer**. For more information, see [Filtering conversations](/docs/watson-assistant?topic=watson-assistant-analytics-conversations#analytics-conversations-filtering).

Filter actions by name
:   You can now find actions more easily. On the Actions page, you can filter actions by name. Click the search icon, then enter a search string. Your list of actions filters to match what you enter.

## 12 August 2022
{: #watson-assistant-aug122022}
{: release-note}

Actions templates
:   When creating actions, you can choose a template that relates to the problem you’re trying to solve. Templates help tailor your actions to include items specific to your business need. The examples in each template can also help you to learn how actions work. Actions templates include features such as intents, entities, condition-based responses, synonyms, response validations, and agent fallback. For more information, see [Building actions from a template](/docs/watson-assistant?topic=watson-assistant-actions-templates).

Channel name variable
:   The `Channel name` integration variable lets you add step conditions using these channels: web chat, phone, SMS, WhatsApp, Slack, or Facebook Messenger. For more information, see [Adding conditions to a step](/docs/watson-assistant?topic=watson-assistant-step-conditions).

## 11 August 2022
{: #watson-assistant-aug112022}
{: release-note}

Algorithm version options available in more languages
:   Algorithm version options are now available in Arabic, Czech, and Dutch. This allows you to choose which {{site.data.keyword.conversationshort}} algorithm to apply to your future trainings. For more information, see [Algorithm version](/docs/watson-assistant?topic=watson-assistant-algorithm-version).

## 9 August 2022
{: #watson-assistant-aug092022}
{: release-note}

New API methods
:   The v2 API now supports new **Environments** and **Releases** methods:

    - **Environments**: Retrieve information about the environments associated with an assistant.

    - **Releases**: Retrieve information about the releases (versions) that have been published for an assistant, and assign an available release to an environment.

For more information, see the v2 [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v2){: external}.

## 5 August 2022
{: #watson-assistant-aug052022}
{: release-note}

Initial value of session variables
:   You can now set the initial value of a session variable to an expression. For more information, see [Creating a session variable](/docs/watson-assistant?topic=watson-assistant-manage-info#create-session-variable).

Uploading intents
:   If you created intents in the classic {{site.data.keyword.conversationshort}} experience, you can migrate your intents to actions in the new {{site.data.keyword.conversationshort}} experience. This can provide a helpful starting point when you are ready to start building actions in the new experience. For more information, see [Uploading intents as actions](/docs/watson-assistant?topic=watson-assistant-manage-actions#manage-actions-upload-intents).

## 19 July 2022
{: #watson-assistant-jul192022}
{: release-note}

Changes to publishing and environments
:   You can now publish versions of your content without assigning to the live environment, allowing you to make continuous updates before customers see it in production. Also, the formerly separate pages for your draft and live environments now appear as tabs on a single *Environments* page, from which you can set up unique configurations for building and testing in the draft environment, and for your customers in the live environment. For more information, see the [Publishing overview](/docs/watson-assistant?topic=watson-assistant-publish-overview).

Logs reader role
:   Identity and Access Management now includes a new service role, **Logs Reader**, which lets you grant access to Analytics without assigning the Manager role. Use Logs Reader in combination with the Reader or Writer role to provide access to the Analytics page. For more information, see [Managing access](/docs/watson-assistant?topic=watson-assistant-access-control).

## 15 July 2022
{: #watson-assistant-jul152022}
{: release-note}

Segment extension
:   The Segment extension is now available for Enterprise plans. With this extension, you can use [Segment](https://segment.com/){: external} to capture and centralize data about your customers' behavior, including their interactions with your assistant. For more information, see [Sending events to Segment](/docs/watson-assistant?topic=watson-assistant-segment-add).

New expression property
:   You can now use the `.literal` property to return the exact response that a customer specifies. This property is helpful if a customer uses a synonym of an option, and you want your assistant to respond with the exact phrase they specified. To set this property, click the **Set variable values** icon and assign a session variable to the step variable. Add the `.literal` property to the step variable. Use the session variable in the assistant's response to display the customer's input.

    For example, suppose you have an option called `plant` that has `fern` as a synonym. A customer might say `buy a fern`. In this case, you can use the `.literal` property so the assistant's response uses the customer's input. Your assistant might respond, `Great! I see you want to buy a fern.`

## 11 July 2022
{: #watson-assistant-jul112022}
{: release-note}

Ability to duplicate an action
:   You can duplicate an action to reuse information in a new action. When you duplicate an action, the new action includes everything except example phrases. Click the overflow menu on the action you want and select **Duplicate**.

New demo site
:   Explore our [interactive demo site](https://www.ibm.com/products/watson-assistant/demos/lendyr/demo.html){: external} to learn how {{site.data.keyword.conversationshort}} can be used to build powerful, scalable experiences for your users.

## 24 June 2022
{: #watson-assistant-jun242022}
{: release-note}

Algorithm version options available in more languages
:   Algorithm version options are now available in Chinese (Traditional), Japanese, and Korean. This allows you to choose which {{site.data.keyword.conversationshort}} algorithm to apply to your future trainings. For more information, see [Algorithm version](/docs/watson-assistant?topic=watson-assistant-algorithm-version).

## 16 June 2022
{: #watson-assistant-jun162022}
{: release-note}

Algorithm version
:   Algorithm version allows you to choose which {{site.data.keyword.conversationshort}} algorithm to apply to your future trainings. For more information, see [Algorithm version](/docs/watson-assistant?topic=watson-assistant-algorithm-version).

Algorithm beta version (2022-06-10)
:   Algorithm beta version (2022-06-10) includes a new irrelevance detection algorithm to improve off-topic detection accuracy. Utterances with similar meanings are expected to have more similar confidences in comparison to previous irrelevance detection algorithms. For example, the training utterance `please suggest route from times square` has 100% confidence at runtime. Currently in IBM Cloud, the utterance `please suggest route from central park` gets a low confidence and could be flagged as irrelevant. With beta version (2022-06-10), the same utterance is expected to be predicted correctly with a ~46% confidence.

## 3 June 2022
{: #watson-assistant-jun032022}
{: release-note}

Extensions support for importing API document with unsupported methods
:   When building a custom extension, you can now import an API document even if it contains operations with required array parameters, which are not supported. The unsupported operations are automatically disabled, but this does not affect other operations. (Previously, the entire API document was rejected if it contained unsupported operations.) For more information, see [Building a custom extension](/docs/watson-assistant?topic=watson-assistant-build-custom-extension).

## 27 May 2022
{: #watson-assistant-may272022}
{: release-note}

Support for custom extensions and dialog in Actions preview panel
:   You can now view your entire assistant from the **Actions preview** panel, including custom extensions and dialog. This allows you to have a complete view of how an action is working. For more information about previewing actions, see [Reviewing and debugging your actions](/docs/watson-assistant?topic=watson-assistant-review).

## 19 May 2022
{: #watson-assistant-may192022}
{: release-note}

Sign out due to inactivity setting
:   {{site.data.keyword.conversationshort}} now uses the **Sign out due to inactivity setting** from Identity & Access Management (IAM). {{site.data.keyword.cloud_notm}} account owners can select the time it takes before an inactive user is signed out and their credentials are required again. The default is 2 hours.

   An inactive user will see two messages. The first message alerts them about an upcoming session expiration and provides a choice to renew. If they remain inactive, a second session expiration message appears and they will need to log in again.

   For more information, see [Setting the sign out due to inactivity duration](/docs/account?topic=account-iam-work-sessions&interface=ui#sessions-inactivity){: external}.

## 12 May 2022
{: #watson-assistant-may122022}
{: release-note}

Ability to upload and download example phrases and upload saved customer responses
:   You can now upload and download example phrases from **Customer starts with** at the start of an action. This can be useful if you have a large number of example phrases and don't want to define them one by one. For more information, see [Adding more examples](/docs/watson-assistant?topic=watson-assistant-understand-questions#understand-questions-adding-more-examples).

   You can also now upload saved customer responses from the **Saved responses** page. For more information, see [Uploading saved customer responses](/docs/watson-assistant?topic=watson-assistant-collect-info#uploading-saved-customer-response).

   The ability to upload example phrases and saved customer responses is also helpful if you're using the classic {{site.data.keyword.conversationshort}} and want to migrate your intents and entities to the new {{site.data.keyword.conversationshort}}. For more information, see [Migrating intents and entities](/docs/watson-assistant?topic=watson-assistant-migrate-intents-entities).

## 5 May 2022
{: #watson-assistant-may052022}
{: release-note}

Success/failure variable for extensions
:   Each call to a custom extension now returns a `Ran successfully` response variable, which you can use to check the success or failure of the call. For more information, see [Checking success or failure](/docs/watson-assistant?topic=watson-assistant-call-extension#extension-check-success).

## 28 April 2022
{: #watson-assistant-apr282022}
{: release-note}

Definitive calculation for abandoned actions
:   Abandonment is now definitively calculated for your actions. On the **Analytics** page, actions are no longer considered `Ongoing` in the action completion analysis. An action is considered abandoned if it was not completed after 1 hour of inactivity and doesn't meet the criteria for any other incompletion reason (escalated to agent, started a new action, or stuck on a step). This change applies only to actions data after April 26, 2022. For more information about action incompletion, see [Reasons for incompletion](/docs/watson-assistant?topic=watson-assistant-analytics-action-completion#incomplete-reasons).

Managing operations in extensions
:   When you add a custom extension to an assistant, you can now choose which operations and response properties will be available to actions. For more information, see [Adding an extension to your assistant](/docs/watson-assistant?topic=watson-assistant-add-custom-extension).

## 21 April 2022
{: #watson-assistant-apr212022}
{: release-note}

Ability to duplicate a step
:   You can now duplicate a step so you don't have to re-create variable settings and customizations. Duplicating a step is helpful when you need to add a step similar to a previous step, but with minor modifications. For more information about how to duplicate a step, see [Duplicating a step](/docs/watson-assistant?topic=watson-assistant-build-actions-overview#build-actions-overview-duplicate-step).

Markdown supported in action editor
:   The action editor now supports basic Markdown syntax. As you type, the action editor renders the Markdown so you can see the content as your customers will when they interact with the assistant.

## 5 April 2022
{: #watson-assistant-apr052022}
{: release-note}

Dialog feature available
:   The dialog feature is available. If you have a dialog-based assistant that was built using the classic {{site.data.keyword.conversationshort}}, you can now migrate your dialog skill to the new {{site.data.keyword.conversationshort}} experience. For more information, see [Migrating to the new experience](/docs/watson-assistant?topic=watson-assistant-migrate-overview).

## 28 March 2022
{: #watson-assistant-mar282022}
{: release-note}

New service desk support reference implementation
:   You can use the reference implementation details to integrate the web chat with the Kustomer service desk. For more information, see [Adding service desk support](/docs/watson-assistant?topic=watson-assistant-deploy-web-chat#deploy-web-chat-haa).

## 18 March 2022
{: #watson-assistant-mar182022}
{: release-note}

Custom extensions
:   If you need to integrate your assistant with an external service that has a REST API, you can now build a custom extension by importing an OpenAPI document. Your assistant can then send requests to the external service and receive response data it can use in the conversation. For example, you might use an extension to interact with a ticketing or customer relationship management (CRM) system, or to retrieve real-time data such as mortgage rates or weather conditions.

   For more information about custom extensions, see [Building a custom extension](/docs/watson-assistant?topic=watson-assistant-build-custom-extension) and [Calling a custom extension](/docs/watson-assistant?topic=watson-assistant-call-extension).

Confirmation customer response type
:   The confirmation customer response type is now available. Use this response type when a customer's response must be either Yes or No. For more information, see [Confirmation](/docs/watson-assistant?topic=watson-assistant-collect-info#customer-response-type-confirmation).

Search integration highlights text in browser
:   Search results in {{site.data.keyword.conversationshort}} include a link. Now, when a customer clicks the link, search results are highlighted in their browser so it’s easier for them to see the relevant content. This feature is supported on Chromium browsers, including Google Chrome and Microsoft Edge.

## 24 February 2022
{: #watson-assistant-feb242022}
{: release-note}

Regex customer response type
:   The regex customer response type is now available. Use this response type to capture a value that must conform to a particular pattern or format, such as an email address or telephone number. For more information, see [Regex](/docs/watson-assistant?topic=watson-assistant-collect-info#customer-response-type-regex).

## 17 February 2022
{: #watson-assistant-feb172022}
{: release-note}

Adding users from the Manage menu
:   If you want to collaborate with others on your assistants, you can now quickly add users with Administrator and Manager access from the **Manage** menu in your assistant. For more information, see [Adding users from the Manage menu](/docs/watson-assistant?topic=watson-assistant-access-control#access-control-add-users).

Preview page share link
:   When you use the **Copy link to share** button to share your assistant, the shared assistant now mirrors the Preview page. If you share the assistant with a colleague, they are able to see the assistant with any customizations that you made on the Preview page.

## 10 February 2022
{: #watson-assistant-feb102022}
{: release-note}

Links in assistant responses can be configured to open in a new tab
:   When you build an action, your assistant responses can include links. If you're using web chat, you can now control whether the link opens in a new tab. To enable a link to open in a new tab, select **Open link in new tab** from the **Insert link** configuration window. For more information, see [Adding assistant responses](/docs/watson-assistant?topic=watson-assistant-respond).

## 9 February 2022
{: #watson-assistant-feb092022}
{: release-note}

All instances now default to new experience
:    All new instances of {{site.data.keyword.conversationshort}} now direct users to the new product experience by default.

    {{site.data.keyword.conversationshort}} has been completely overhauled to simplify the end-to-end process of building and deploying a virtual assistant, reducing time to launch and enabling nontechnical authors to create virtual assistants without involving developers. For more information about the new {{site.data.keyword.conversationshort}}, and instructions for switching between the new and old experiences, see [Welcome to the new {{site.data.keyword.conversationshort}}](/docs/watson-assistant?topic=watson-assistant-welcome-new-assistant).

    If you would like to send us feedback on the new experience, please use [this form](https://form.asana.com/?k=vvRdQAmGMFAeEGRryhTA2w&d=8612789739828){: external}.

## 3 February 2022
{: #watson-assistant-feb032022}
{: release-note}

Customize the Preview page background
:   You can now change the background of the **Preview** page to one of your organization's web pages so you can preview and test your assistant from a customer's perspective. For more information, see [Previewing and sharing your assistant](/docs/watson-assistant?topic=watson-assistant-preview-share).

Add a type to session variables
:   When you create a session variable, you can now assign a type to the variable. For more information, see [Creating a session variable](/docs/watson-assistant?topic=watson-assistant-manage-info#create-session-variable). After a type is assigned to a variable, you can set more explicit conditions on that variable. Previously, you were able to check only whether session variables were `defined` or `not defined`. With variable types, you can create conditions based on the type of the variable (for example, `account balance < 100` or `departure date is after today`). For more information, see [Operators](/docs/watson-assistant?topic=watson-assistant-step-conditions#operators).

Create saved customer responses
:   You can now create saved customer responses. There might be some questions that your assistant needs to ask in different steps and actions. For example, a banking assistant might have different actions that ask for a customer's account number. Instead of building the same response over and over, you can create a saved customer response and reuse it across steps in multiple actions. For more information, see [Saving and reusing customer responses](/docs/watson-assistant?topic=watson-assistant-collect-info#saved-customer-responses).

## 13 January 2022
{: #watson-assistant-jan132022}
{: release-note}

New setting for options customer response type
:    In actions, a new **List options** setting allows you to enable or disable the options customer response from appearing in a list. This can be useful to prevent a phone integration from reading a long list of options to the customer. As part of this change, all customer response types now have a **Settings** icon. **Allow skipping** has moved from **Edit Response** and is now found in the new settings. For more information, see [Collecting information from your customers](/docs/watson-assistant?topic=watson-assistant-collect-info).

## 24 December 2021
{: #watson-assistant-dec242021}
{: release-note}

Apache Log4j security vulnerability updates
:   {{site.data.keyword.conversationshort}} upgraded to using Log4j version 2.17.0, which addresses all of the Critical severity and High severity Log4j CVEs, specifically CVE-2021-45105, CVE-2021-45046, and CVE-2021-44228.

## 3 December 2021
{: #watson-assistant-dec032021}
{: release-note}

Configure webhook timeout
:   From the **Pre-message webhook** and **Post-message webhook** configuration pages, you can configure the webhook timeout length from a minimum of 1 second to a maximum of 30 seconds. For more information, see [Extending your assistant with webhooks](/docs/watson-assistant?topic=watson-assistant-webhook-overview).

User-based switching between {{site.data.keyword.conversationshort}} experiences
:   Previously, switching between the new {{site.data.keyword.conversationshort}} experience and the classic {{site.data.keyword.conversationshort}} experience was instance-based. For example, if a user switched from the classic experience to the new experience, all users of that {{site.data.keyword.conversationshort}} instance were switched to the new experience. Now, switching between the experiences is user-based. So, any user of a {{site.data.keyword.conversationshort}} instance can switch between the new and classic experiences, and other users of that {{site.data.keyword.conversationshort}} instance are not affected.

## 27 November 2021
{: #watson-assistant-nov272021}
{: release-note}

New API version
:   The current API version is now `2021-11-27`. This version introduces the following changes:

    - The `output.text` object is no longer returned in `message` responses. All responses, including text responses, are returned only in the `output.generic` array.

## 12 November 2021
{: #watson-assistant-nov122021}
{: release-note}

Completion analytic information
:   On the **Analyze** page, the **How often** chart can now also show the percentage of complete actions. Use the icon in the upper right of the chart to toggle between a line chart that shows the percentage of complete actions and a bar chart that shows the number of complete and incomplete actions. For more information, see [Improving completion](/docs/watson-assistant?topic=watson-assistant-analytics-action-completion#analytics-improving-completion).

Preview page update
:   The **Test integrations** panel no longer exists on the **Preview** page. You can manage your draft web chat channel from the **Preview** page. However, all other draft environment integrations are managed from the **Draft environment** page. For more information, see [Previewing and sharing your assistant](/docs/watson-assistant?topic=watson-assistant-preview-share).

## 4 November 2021
{: #watson-assistant-nov042021}
{: release-note}

Draft and Live Environment pages
:   Two pages, **Draft environment** and **Live environment**, help you to see how your channels and resolution methods are connected, both for testing/preview and for live deployment. The Draft environment page is new as of this release. The Live environment page was previously named Connect. For more information, see [Overview: Publishing and deploying your assistant](/docs/watson-assistant?topic=watson-assistant-publish-overview).

Add variables to links
:   When including a link in an assistant response, you can now access and use variables. In the URL field for a link, type a dollar sign (`$`) character to see a list of variables to choose from.

## 25 October 2021
{: #watson-assistant-oct252021}
{: release-note}

Facebook and Slack integrations now available
:   The new Watson Assistant now includes integrations for [Facebook Messenger](/docs/watson-assistant?topic=watson-assistant-deploy-facebook) and [Slack](/docs/watson-assistant?topic=watson-assistant-deploy-slack).

Analytics for draft and live environments
:   The **Analyze** page now lets you see analytics data for either the draft or live environments. For more information, see [Use analytics to review your entire assistant at a glance](/docs/watson-assistant?topic=watson-assistant-analytics-overview).

## 7 October 2021
{: #watson-assistant-oct072021}
{: release-note}

The new Watson Assistant
:   The new Watson Assistant is now available! This new experience, focused on using **actions** to build customer conversations, is designed to make it simple enough for *anyone* to build a virtual assistant. Building, testing, publishing, and analyzing your assistant can all now be done in one simple and intuitive interface.

    - New **navigation** provides a workflow for building, previewing, publishing, and analyzing your assistant.
    - Each assistant has a **home page** with a task list to help you get started.
    - Build conversations with **actions**, which represent the tasks you want your assistant to help your customers with. Each action contains a series of steps that represent individual exchanges with a customer.
    - A new way to **publish** lets you review and debug your work in a draft environment before going live to your customers.
    - Use a new suite of **analytics** to improve your assistant. Review which actions are being completed to see what your customers want help with, determine if your assistant understands and addresses customer needs, and decide how can you make your assistant better.
    - New **[documentation](/docs/watson-assistant)** focuses on the workflow of building, deploying, and improving your assistant.

Older release notes might link to the [documentation for the classic Watson Assistant experience](/docs/assistant){: external}.

## 21 September 2021
{: #watson-assistant-sep212021}
{: release-note}

Analytics Overview change
:   To improve reliability, the Values column has been removed from **Top entities** on the **Analytics Overview** page. Top Entities continues to provide counts of entity types. For more information, see [Top intents and top entities](/docs/assistant?topic=assistant-logs-overview#logs-overview-tops){: external}

## 16 September 2021
{: #watson-assistant-sep162021}
{: release-note}

Enhanced intent detection for French, Italian, and Spanish dialog skills
:   The new intent detection model improves your assistant's ability to understand what customers want. This model is now available in dialog skills using French, Italian, and Spanish. For more information, see [Improved intent recognition](/docs/assistant?topic=assistant-intent-detection){: external}.

Change to the irrelevance detection option
:   As of this release, new English dialog skills no longer include the option to choose between the **Enhanced** or **Existing** irrelevance detection. By default, intent detection and irrelevance detection are paired like this:

    - If you use the dialog skill options to choose enhanced intent detection, it is automatically paired with enhanced irrelevance detection.
    - If you use the dialog skill options to choose existing intent detection, it is automatically paired with existing irrelevance detection.

    For more information, see [Defining what's irrelevant](/docs/assistant?topic=assistant-irrelevance-detection){: external} and [Improved intent recognition](/docs/assistant?topic=assistant-intent-detection){: external}.

    If necessary, you can use the [Update workspace API](/apidocs/assistant/assistant-v1?curl=#updateworkspace){: external} to set your English-language assistant to one of the four combinations of intent and irrelevance detection:

    - Enhanced intent recognition and enhanced irrelevance detection
    - Enhanced intent recognition and existing irrelevance detection
    - Existing intent recognition and enhanced irrelevance detection
    - Existing intent recognition and existing irrelevance detection

    For French, Italian, and Spanish, you can use the API to set your assistant to these combinations:
    - Enhanced intent recognition and enhanced irrelevance detection
    - Existing intent recognition and existing irrelevance detection

## 15 September 2021
{: #watson-assistant-sep152021}
{: release-note}

Dialog skill "Try it out" improvements
:   The **Try it out** pane now includes these changes:

    - It now includes runtime warnings in addition to runtime errors.

    - For dialog skills, the **Try it out** pane now uses the [React](https://reactjs.org/){: external} UI framework similar to the rest of the {{site.data.keyword.conversationshort}} user interface. You shouldn't see any change in behavior or functionality. As a part of the update, dialog skill error handling has been improved within the "Try it out" pane. This update was enabled on these dates:

        - September 9, 2021 in the Tokyo and Seoul data centers
        - September 13, 2021 in the London, Sydney, and Washington, D.C. data centers
        - September 15, 2021 in the Dallas and Frankfurt data centers

## 13 September 2021
{: #watson-assistant-sep132021}
{: release-note}

Dialog skill "Try it out" improvements
:   For dialog skills, the **Try it out** pane now uses the [React](https://reactjs.org/){: external} UI framework similar to the rest of the {{site.data.keyword.conversationshort}} user interface. You shouldn't see any change in behavior or functionality. As a part of the update, dialog skill error handling has been improved within the "Try it out" pane. This update was enabled on September 9, 2021 in the Tokyo and Seoul data centers. On September 13, 2021, the update was enabled in the London, Sydney, and Washington, D.C. data centers.

Disambiguation feature updates
:   The dialog skill disambiguation feature now includes improved features:

    - **Increased control**: The frequency and depth of disambiguation can now be controlled by using the **sensitivity** parameter in the [workspace API](/apidocs/assistant/assistant-v1#updateworkspace){: external}. There are 5 levels of sensitivity:
        - `high`
        - `medium_high`
        - `medium`
        - `medium_low`
        - `low`

        The default (`auto`) is `medium_high` if this option is not set.

    - **More predictable**: The new disambiguation feature is more stable and predictable. The choices shown may sometimes vary slightly to enable learning and analytics, but the order and depth of disambiguation is largely stable.

    These new features may affect various metrics, such as disambiguation rate and click rates, as well as influence conversation-level key performance indicators such as containment.

    If the new disambiguation algorithm works differently than expected for your assistant, you can adjust it using the sensitivity parameter in the update workspace API. For more information, see [Update workspace](/apidocs/assistant/assistant-v1#updateworkspace){: external}.

## 9 September 2021
{: #watson-assistant-sep092021}
{: release-note}

Actions skill improvements
:   Actions skills now include these new features:

    - **Change conversation topic**: In general, an action is designed to lead a customer through a particular process without any interruptions. In real life, however, conversations almost never follow such a simple flow. In the middle of a conversation, customers might get distracted, ask questions about related issues, misunderstand something, or just change their minds about what they want to do. The **Change conversation topic** feature enables your assistant to handle these digressions, dynamically responding to the user by changing the conversation topic as needed. For more information, see [Changing the topic of the conversation](/docs/assistant?topic=assistant-actions#actions-change-topic){: external}.

    - **Fallback action**: The built-in action, *Fallback*, provides a way to automatically connect customers to a human agent if they need more help. This action helps you to handle errors in the conversation, and is triggered by these conditions:
        - Step validation failed: The customer repeatedly gave answers that were not valid for the expected customer response type.
        - Agent requested: The customer directly asked to be connected to a human agent.
        - No action matches: The customer repeatedly made requests or asked questions that the assistant did not understand.

        For more information, see [Set by assistant actions](/docs/assistant?topic=assistant-actions#actions-builtin){: external}.


Dialog skill "Try it out" improvements
:   For dialog skills, the **Try it out** pane now uses the [React](https://reactjs.org/){: external} UI framework similar to the rest of the {{site.data.keyword.conversationshort}} user interface. You shouldn't see any change in behavior or functionality. As a part of the update, dialog skill error handling has been improved within the "Try it out" pane. This update will be implemented incrementally, starting with service instances in the Tokyo and Seoul data centers.

## 2 September 2021
{: #watson-assistant-sep022021}
{: release-note}

Deploy your assistant on the phone in minutes
:   We have partnered with [IntelePeer](https://intelepeer.com/){: external} to enable you to generate a phone number for free within the phone integration. Simply choose to generate a free number when following the prompts to create a phone integration, finish the setup, and a number is assigned to your assistant. These numbers are robust and ready for production.

Connect to your existing service desks
:   We have added step-by-step documentation for connecting to [Genesys](/docs/assistant?topic=assistant-deploy-phone-genesys){: external} and [Twilio Flex](/docs/assistant?topic=assistant-deploy-phone-flex){: external} over the phone. Easily hand off to your live agents when your customers require telephony support from your service team. {{site.data.keyword.conversationshort}} deploys on the phone via SIP, so most phone based service desks can easily be integrated via SIP trunking standards.

## 23 August 2021
{: #watson-assistant-aug232021}
{: release-note}

Intent detection updates
:   Intent detection for the English language has been updated with the addition of new word-piece algorithms. These algorithms improve tolerance for out-of-vocabulary words and misspelling. This change affects only English-language assistants, and only if the enhanced intent recognition model is enabled. (For more information about the enhanced intent recognition model, and how to determine whether it is enabled, see [Improved intent recognition](/docs/assistant?topic=assistant-intent-detection){: external}.)

Automatic retraining of old skills and workspaces
:   As of August 23, 2021, {{site.data.keyword.conversationshort}} enabled automatic retraining of existing skills in order to take advantage of updated algorithms. The {{site.data.keyword.conversationshort}} service will continually monitor all ML models, and will automatically retrain those models that have not been retrained within the previous 6 months. For more information, see [Automatic retraining of old skills and workspaces](/docs/assistant?topic=assistant-skill-auto-retrain){: external}.

## 19 August 2021
{: #watson-assistant-aug192021}
{: release-note}

Actions preview now includes debug mode and variable values
:   When previewing your actions, you can use **debug mode** and **variable values** to ensure your assistant is working the way you expect.

    **Debug mode** allows you to go to the corresponding step by clicking on a step locator next to each message. It shows you the confidence score of top three possible action when the input triggers an action. You can also follow the step in the action editor along with the conversation flow.

    **Variable values** shows you a list of the variables and their values of current action and the session variables. You can check and edit variables during the conversation flow.

## 17 August 2021
{: #watson-assistant-aug172021}
{: release-note}

New service desk support reference implementation
:   You can use the reference implementation details to integrate the web chat with the Oracle B2C Service service desk. For more information, see [Adding service desk support](/docs/assistant?topic=assistant-deploy-web-chat#deploy-web-chat-haa){: external}.

## 29 July 2021
{: #watson-assistant-jul292021}
{: release-note}

Salesforce and Zendesk deployment changes
:   The Salesforce and Zendesk integrations have been updated to use the [new chat history widget](/docs/assistant?topic=assistant-release-notes-chat#4.5.0){: external}. The updated deployment process applies to all new deployments, including any redeployments of existing Salesforce and Zendesk connections. However, existing deployments are not affected and do not need to be modified or redeployed at this time.

Fallback value for session variables
:   In action skills, you can now set a fallback value for session variables. This feature lets you to define a value for a session variable if a user-defined value isn't found. To learn more, see [Defining session variables](/docs/assistant?topic=assistant-actions#actions-variables-global){: external}.

## 16 July 2021
{: #watson-assistant-jul162021}
{: release-note}

Logging API changes
:   The internal storage and processing of logs has changed. Some undocumented fields or filters might no longer be available. (Undocumented features are not officially supported and might change without notice.)

New API version
:   The current API version (v1 and v2) is now `2021-06-14`. The following changes were made with this version:

    - The `metadata` property of entities detected at run time is deprecated. For detailed information about detected system entities, see the `interpretation` property.
    - The data types of certain entity mentions are no longer automatically converted:
        - Numbers in scientific notation (such as `1E10`), which were previously converted to numbers
        - Boolean values (such as `false`), which were previously converted to booleans

    These values are now returned as strings.

## 17 June 2021
{: #watson-assistant-jun172021}
{: release-note}

Actions skill now generally available
:   As of this release, the beta program has ended, and actions skills are available for general use.

    An actions skill contains actions that represent the tasks you want your assistant to help your customers with. Each action contains a series of steps that represent individual exchanges with a customer. Building the conversation that your assistant has with your customers is fundamentally about deciding which steps, or which user interactions, are required to complete an action. After you identify the list of steps, you can then focus on writing engaging content to turn each interaction into a positive experience for your customer. For more information, see [Actions skill overview](/docs/assistant?topic=assistant-actions-overview){: external}.

Date and time response types
:   New to action skills, these response types allow you to collect date and time information from customers as they answer questions or make requests. For more information, see [Response types](/docs/assistant?topic=assistant-actions#actions-response-types){: external}.

New built-in variables
:   Two kinds of built-in variables are now available for action skills.

    - **Set by assistant** variables include the common and essential variables `Now`, `Current time`, and `Current date`.
    - **Set by integration** variables are `Timezone` and `Locale` and are available to use when connected to a webhook or integration.

    For more information, see [Adding and referencing variables](/docs/assistant?topic=assistant-actions#actions-variables){: external}.

Universal language model now generally available
:   You now can build an assistant in any language you want to support. If a dedicated language model is not available for your target language, create a skill that uses the universal language model. The universal model applies a set of shared linguistic characteristics and rules from multiple languages as a starting point. It then learns from training data written in the target language that you add to it. For more information, see [Understanding the universal language model](/docs/assistant?topic=assistant-assistant-language#assistant-language-universal){: external}.

## 3 June 2021
{: #watson-assistant-jun032021}
{: release-note}

Log webhook support for actions and search skills
:   The log webhook now supports messages exchanged with actions skills and search skills, in addition to dialog skills. For more information, see [Logging activity with a webhook](/docs/assistant?topic=assistant-webhook-log){: external}.

## 27 May 2021
{: #watson-assistant-may272021}
{: release-note}

Change to conversation skill choices
:   When adding skills to new or existing assistant, the conversation skill choices have been combined, so that you pick from either an actions skill or a dialog skill.

    With this change:
    - New assistants can use up to two skills, either actions and search or dialog and search. Previously, new assistants could use up to three skills: actions, dialog, and search.
    - Existing assistants that already use an actions skill and a dialog skill together can continue to use both.
    - The ability to use actions and dialog skills together in a new assistant is planned for 2H 2021.

## 20 May 2021
{: #watson-assistant-may202021}
{: release-note}

Actions skill improvement
: Actions now include a new choice, **Go to another action**, for what to do next in a step. This feature lets you can call one action from another action, to switch the conversation flow to another action to perform a certain task. If you have a portion of an action that can be applied across multiple use cases you can build it once and call to it from each action. This new option is available in the **And then** section of each step. For more information, see [Deciding what to do next](/docs/assistant?topic=assistant-actions#actions-what-next){: external}.

## 21 April 2021
{: #watson-assistant-apr212021}
{: release-note}

Preview button for testing your assistant
:   For testing your assistant, the new Preview button replaces the previous Preview tile in Integrations.

New checklist with steps to go live
:   Each assistant includes a checklist that you can use to ensure you're ready to go live.

Actions skill improvement
:   Actions now include currency and percentage response types.

Learn what's new
:   The *What's new* choice on the help menu opens a list of highlighting recent features.

## 14 April 2021
{: #watson-assistant-apr142021}
{: release-note}

Actions skill improvement
:   Actions now include a free text response type, allowing you to capture special instructions or requests that a customer wants to pass along.

## 8 April 2021
{: #watson-assistant-apr082021}
{: release-note}

Deploy your assistant to WhatsApp - now generally available
:   Make your assistant available through Whatsapp messaging so it can exchange messages with your customers where they are. This integration, which is now generally available, creates a connection between your assistant and WhatsApp by using Twilio as a provider. For more information, see [Integrating with WhatsApp](/docs/assistant?topic=assistant-deploy-whatsapp){: external}.

Web chat home screen now generally available
:   Ease your customers into the conversation by adding a home screen to your web chat window. The home screen greets your customers and shows conversation starter messages that customers can click to easily start chatting with the assistant. For more information about the home screen feature, see [Configuring the home screen](/docs/assistant?topic=assistant-deploy-web-chat#deploy-web-chat-home-screen){: external}. The home screen feature is now enabled by default for all new web chat deployments. Also, you can now access context variables from the home screen. Note that initial context must be set using a `conversation_start` node. For more information, see [Starting the conversation](/docs/assistant?topic=assistant-dialog-start#dialog-start-welcome){: external}.

Connect to human agent response type allows more text
:   In a dialog skill, the response type *Connect to human agent* now allows 320 characters in the *Response when agents are online* and *Response when no agents are online* fields. The previous limit was 100 characters.

Legacy system entities deprecated
:   In January 2020, a new version of the system entities was introduced. As of April 2021, only the new version of the system entities is supported for all languages. The option to switch to using the legacy version is no longer available.    

## 6 April 2021
{: #watson-assistant-apr062021}
{: release-note}

Service API endpoint change
:   As explained in [December 2019](#watson-assistant-dec122019), as part of work done to fully support IAM authentication, the endpoint you use to access your {{site.data.keyword.conversationshort}} service programmatically is changing. The old endpoint URLs are deprecated and **will be retired on 26 May 2021**. Update your API calls to use the new URLs.

    The pattern for the endpoint URL changes from `gateway-{location}.watsonplatform.net/assistant/api/` to `api.{location}.assistant.watson.cloud.ibm.com/`. The domain, location, and offering identifier are different in the new endpoint. For more information, see [Updating endpoint URLs from watsonplatform.net](/docs/watson?topic=watson-endpoint-change){: external}.

    - If your service instance API credentials show the old endpoint, create a new credential and start using it today. After you update your custom applications to use the new credential, you can delete the old one.

    - For a web chat integration, you might need to take action depending on when and how you created your integration.

        - If you tied your deployment to a specific web chat version by using the `clientVersion` parameter and specified a version earlier than version 3.3.0, update the parameter value to use version 3.3.0 or later. Web chat integrations that use the latest or 3.3.0 and later versions will not be impacted by the endpoint deprecation.

        - If you created your web chat integration before May 2020, check the code snippet that you embedded in your web page to see if it refers to `watsonplatform.net`. If so, you must edit the code snippet to use the new URL syntax. For example, change the following URL:

            ```html
             <script src="https://assistant-web.watsonplatform.net/loadWatsonAssistantChat.js"></script>
            ```

            The correct syntax to use for the source service URL looks like this:

            ```code
            src="https://web-chat.global.assistant.watson.appdomain.cloud/loadWatsonAssistantChat.js"
            ```

    - If your web chat integration connects to a Salesforce service desk, then you must edit the API call that is included in the code snippet that you added to the Visualforce Page that you created in Salesforce. From Salesforce, search for *Visualforce Pages*, and find your page. In the `<iframe>` snippet that you pasted into the page, make the following change:

      Replace: `src=“https://assistant-integrations-{location}.watsonplatform.net/public/salesforceweb”` with a url with this syntax:

        ```code
        src="https://integrations.{location}.assistant.watson.appdomain.cloud/public/salesforceweb/{integration-id}/agent_application?version=2020-09-24"
        ```
        {: codeblock}

      From the Web chat integration Salesforce live agent setup page, find the *Visualforce page markup* field. Look for the `src` parameter in the `<iframe>` element. It contains the full URL to use, including the appropriate `{location}` and `{integration-id}` values for your instance.

    - For a Slack integration that is over 7 months old, make sure the Request URL is using the proper endpoint.

        - Go to the [Slack API](https://api.slack.com/){: external} web page. Click *Your Apps* to find your assistant app. Click *Event Subscriptions* from the navigation pane.
        - Edit the Request URL.

      For example, if the URL has the syntax: `https://assistant-slack-{location}.watsonplatform.net/public/message`, change it to have this syntax:

      ```code
      https://integrations.{location}.assistant.watson.appdomain.cloud/public/slack/{integration-id}/message?version=2020-09-24
      ```
      {: codeblock}

      Check the *Generated request URL* field in the Slack integration setup page for the full URL to use, which includes the appropriate `{location}` and `{integration-id}` values for your instance.

    - For a Facebook Messenger integration that is over 7 months old, make sure the Callback URL is using the proper endpoint.

        - Go to the [Facebook for Developers](https://developers.facebook.com/apps/){: external} web page.
        - Open your app, and then select *Messenger>Settings* from the navigation pane.
        - Scroll down to the *Webhooks* section and edit the *Callback URL* field.

          For example, if the URL has the syntax: `https://assistant-facebook-{location}.watsonplatform.net/public/message/`, change it to have this syntax:

          ```code
          https://integrations.{location}.assistant.watson.appdomain.cloud/public/facebook/{integration-id}/message?version=2020-09-24
          ```
          {: codeblock}

          Check the *Generated callback URL* field in the Facebook Messenger integration setup page for the full URL to use, which includes the appropriate `{location}` and `{integration-id}` values for your instance.

    - For a Phone integration, if you connect to existing speech service instances, make sure those speech services use credentials that were generated with the latest endpoint syntax (a URL that starts with `https://api.{location}.speech-to-text.watson.cloud.ibm.com/`).

    - For a search skill, if you connect to an existing {{site.data.keyword.discoveryshort}} service instance, make sure the {{site.data.keyword.discoveryshort}} service uses credentials that were generated with the supported syntax (a URL that starts with `https://api.{location}.discovery.watson.cloud.ibm.com/`).

    - If you are using [Jupyter notebooks](/docs/assistant?topic=assistant-logs-resources#logs-resources-jupyter-logs){: external} to do advanced analytics, check your Jupyter notebook files to make sure they don't specify URLs with the old `watsonplatform.net` syntax. If so, update your files.

    - No action is required for the following integration types:

        - Intercom
        - SMS with Twilio
        - WhatsApp with Twilio
        - Zendesk service desk connection from web chat

## 23 March 2021
{: #watson-assistant-mar232021}
{: release-note}

Actions skill improvement
:   Actions have a new toolbar making it easier to send feedback, access settings, save, and close.

## 17 March 2021
{: #watson-assistant-mar172021}
{: release-note}

Channel transfer response type
:   Dialog skills now include a channel transfer response type. If your assistant uses multiple integrations to support different channels for interaction with users, there might be some situations when a customer begins a conversation in one channel but then needs to transfer to a different channel. The most common such situation is transferring a conversation to the web chat integration, to take advantage of web chat features such as service desk integration. For more information, see [Adding a Channel transfer response type](/docs/assistant?topic=assistant-dialog-overview#dialog-overview-add-channel-transfer){: external}.

Intercom and WhatsApp integrations now available in Lite plan
:   The integrations for Intercom and WhatsApp are now available in the Lite plan for {{site.data.keyword.conversationshort}}. For more information, see [Integrating with Intercom](/docs/assistant?topic=assistant-deploy-intercom) and [Integrating with WhatsApp](/docs/assistant?topic=assistant-deploy-whatsapp){: external}.

## 16 March 2021
{: #watson-assistant-mar162021}
{: release-note}

Session history now generally available
:   Session history allows your web chats to maintain conversation history and context when users refresh a page or change to a different page on the same website. It is enabled by default. For more information about this feature, see [Session history](https://web-chat.global.assistant.watson.cloud.ibm.com/docs.html?to=tutorials-session-history){: external}.

    Session history persists within only one browser tab, not across multiple tabs. The dialog provides an option for links to open in a new tab or the same tab. See [this example](https://web-chat.global.assistant.watson.cloud.ibm.com/docs.html?to=tutorials-session-history#Tutorial1){: external} for more information on how to format links to open in the same tab.

    Session history saves changes that are made to messages with the [pre:receive event](https://web-chat.global.assistant.watson.cloud.ibm.com/docs.html?to=api-events#prereceive){: external} so that messages still look the same on rerender. This data is only saved for the length of the session. If you prefer to discard the data, set `event.updateHistory = false;` so the message is rerendered without the changes that were made in the pre:receive event.

    [instance.updateHistoryUserDefined()](https://web-chat.global.assistant.watson.cloud.ibm.com/docs.html?to=api-instance-methods#updateHistoryUserDefined){: external} provides a way to save state for any message response. With the state saved, a response can be rerendered with the same state. This saved state is available in the `history.user_defined` section of the message response on reload. The data is saved during the user session. When the session expires, the data is discarded.

    Two new history events, [history:begin](https://web-chat.global.assistant.watson.cloud.ibm.com/docs.html?to=api-events#historybegin){: external} and [history:end](https://web-chat.global.assistant.watson.cloud.ibm.com/docs.html?to=api-events#historyend){: external} announce the beginning and end of the history of a reloaded session. These events can be used to view the messages that are being reloaded. The history:begin event allows you to edit the messages before they are displayed.

    See this example for more information on saving the state of [customResponse](https://web-chat.global.assistant.watson.cloud.ibm.com/testfest.html?to=api-events#customresponse){: external} types in session history.

Channel switching
:   You can now create a dialog response type to functionally generate a connect-to-agent response within channels other than web chat. If a user is in a channel such as Slack or Facebook, they can trigger a channel transfer response type. The user receives a link that forwards them to your organization's website where a connection to an agent response can be started within web chat. For more information, see [Adding a Channel transfer response type](/docs/assistant?topic=assistant-dialog-overview#dialog-overview-add-channel-transfer){: external}.

## 11 March 2021
{: #watson-assistant-mar112021}
{: release-note}

Actions skill improvement
:   Updated the page where you configure a step with an *Options* reply constraint. Now it's clearer that you have a choice to make about whether to always ask for the option value or to skip asking. For more information, see [Apply reply constraints](/docs/assistant?topic=assistant-actions#actions-response-types){: external}.

## 4 March 2021
{: #watson-assistant-mar042021}
{: release-note}

Support for every language!
:   You now can build an assistant in any language you want to support. If a dedicated language model is not available for your target language, create a skill that uses the universal language model. The universal model applies a set of shared linguistic characteristics and rules from multiple languages as a starting point. It then learns from training data written in the target language that you add to it.

    The universal model is available as a beta feature. For more information, see [Understanding the universal language model](/docs/assistant?topic=assistant-assistant-language#watson-assistant-language-universal){: external}.

Actions skill improvement
:   Now you can indicate whether or not to ask for a number when you apply a number reply constraint to a step. Test how changes to this setting might help speed up a customer's interaction. Under the right circumstances, it can be useful to let a number mention be recognized and stored without having to explicitly ask the customer for it. For more information, see [Applying reply constraints](/docs/assistant?topic=assistant-actions#actions-response-types){: external}.

## 1 March 2021
{: #watson-assistant-mar012021}
{: release-note}

Introducing the *Enterprise* plan!
:   The Enterprise plan includes all of the market differentiating features of the Plus plan, but with higher capacity limits, additional security features, custom onboarding support to get you going, and a lower overall cost at higher volumes.

    To have a dedicated environment provisioned for your business, request the *Enterprise with Data Isolation* plan. To submit a request online, go to [http://ibm.biz/contact-wa-enterprise](http://ibm.biz/contact-wa-enterprise){: external}.

    The Enterprise plan is replacing the Premium plan. The Premium plan is being retired today. Existing Premium plan users are not impacted. They can continue to work in their Premium instances and create instances up to the 30-instance limit. New users do not see the Premium plan as an option when they create a service instance.

    For more information, see the [Pricing](https://www.ibm.com/cloud/watson-assistant/pricing/){: external} page.

Other plan changes
:   Our pricing has been revised to reflect the features we've added that help you build an assistant that functions as a powerful omnichannel SaaS application.

    Starting on 1 March 2021, the Plus plan starts at $140 per month and includes your first 1,000 monthly users. You pay $14 for each additional 100 active users per month. Use of the voice capabilities that are provided by the *Phone* integration are available for an additional $9 per 100 users per month.

    The Plus Trial plan was renamed to Trial.

SOC 2 compliance
:   {{site.data.keyword.conversationshort}} is SOC 2 Type 2 compliant, so you know your data is secure.

    The System and Organization Controls framework, developed by the American Institute of Certified Public Accountants (AICPA), is a standard for controls that protect information stored in the cloud. SOC 2 reports provide details about the nature of internal controls that are implemented to protect customer-owned data. For more information, see [IBM Cloud compliance programs](https://www.ibm.com/cloud/compliance/global){: external}.

## 25 February 2021
{: #watson-assistant-feb252021}
{: release-note}

Search skill can emphasize the answer
:   You can configure the search skill to highlight text in the search result passage that {{site.data.keyword.discoveryshort}} determines to be the exact answer to the customer's question. For more information, see [Creating a search skill](/docs/assistant?topic=assistant-skill-search-add){: external}.

Integration changes
:   The following changes were made to the integrations:

    - The name of *Preview link* integration changed to *Preview*.
    - The *Web chat* and *Preview* integrations are no longer added automatically to every new assistant.

        The integrations continue to be added to the *My first assistant* that is generated for you automatically when you first create a new service instance.

Message and log webhooks are generally available
:   The premessage, postmessage, and log webhooks are now generally available. For more information about them, see [Webhook overview](/docs/assistant?topic=assistant-webhook-overview){: external}.

## 11 February 2021
{: #watson-assistant-feb112021}
{: release-note}

The `user_id` value is easier to access
:   The `user_id` property is used for billing purposes. Previously, it was available from the context object as follows:

    - v2: `context.global.system.user_id`
    - v1: `context.metadata.user_id`

    The property is now specified at the root of the `/message` request in addition to the context object. The built-in integrations typically set this property for you. If you're using a custom application and don't specify a `user_id`, the `user_id` is set to the `session_id` (v2) or `conversation_id`(v1) value.

Digression bug fix
:   Fixed a bug where digression setting changes that were made to a node with slots were not being saved.

## 5 February 2021
{: #watson-assistant-feb052021}
{: release-note}

Documentation update
:   The phone and *SMS with Twilio* deployment documentation was updated to include instructions for migrating from {{site.data.keyword.iva_short}}. For more information, see [Integrating with phone](/docs/assistant?topic=assistant-deploy-phone#deploy-phone-migrate-from-va){: external} and [Integrating with *SMS with Twilio*](/docs/assistant?topic=assistant-deploy-sms#deploy-sms-migrate-from-va){: external}.

## 27 January 2021
{: #watson-assistant-jan272021}
{: release-note}

Language support was expanded for intent recommendations
:   The intent recommendations feature is now supported in Brazilian Portuguese, French, German, Italian, and Spanish dialog skills. For more information, see [Supported languages](/docs/assistant?topic=assistant-language-support){: external}.

German language improvements
:   A word decomposition function was added to the intent and entity recognition models for German-language dialog skills.

    A characteristic of the German language is that some words are formed by concatenating separate words to form a single compound word. For example, "festnetznummer" (landline number) concatenates the words "festnetz" (landline) and "nummer" (number). When your customers chat with your assistant, they might write a compound word as a single word, as hyphenated words, or as separate words. Previously, the variants resulted in different intent confidence scores and different entity mention counts based on your training data. With the addition of the word decomposition function, the models now treat all compound word variants as equivalent. This update means you no longer need to add examples of every variant of the compound words to your training data.

## 19 January 2021
{: #watson-assistant-jan192021}
{: release-note}

The *Phone* and *SMS with Twilio* integrations are now generally available!
:   For more information, see:

    - [Integrating with phone](/docs/assistant?topic=assistant-deploy-phone){: external}
    - [Integrating with *SMS with Twilio*](/docs/assistant?topic=assistant-deploy-sms){: external}

*Preview link* change
:   When you create a preview link, you can now test your skill from a chat window that is embedded in the page. You can also copy the URL that is provided, and open it in a web browser to see an IBM-branded web page with the web chat embedded in it. You can share the URL to the public IBM web page with others to get help with testing or for demoing purposes. For more information, see [Testing your assistant](/docs/assistant?topic=assistant-deploy-web-link){: external}.

Import and export UI changes
:   The label on buttons for importing skills changed from *Import* to *Upload*, and the label on buttons for exporting skills changed from *Export* to *Download*.

Coverage metric change
:   The coverage metric now looks for nodes that were processed with a node condition that includes the `anything_else` special condition instead of nodes that are named `Anything else`. For more information, see [Starting and ending the dialog](/docs/assistant?topic=assistant-dialog-start){: external}.

## 15 January 2021
{: #watson-assistant-jan152021}
{: release-note}

Use new webhooks to process messages!
:   A set of new webhooks is available as a beta feature. You can use the webhooks to perform preprocessing tasks on incoming messages and postprocessing tasks on the corresponding responses. You can use the new log webhook to log each message with an external service. For more information, see [Webhook overview](/docs/assistant?topic=assistant-webhook-overview){: external}.

New service desk support reference implementation
:   You can use the reference implementation details to integrate the web chat with the NICE inContact service desk. For more information, see [Adding service desk support](/docs/assistant?topic=assistant-deploy-web-chat#deploy-web-chat-haa){: external}.

Phone and *SMS with Twilio* integration updates
:   The phone integration now enables you to specify more than one phone number, and the numbers can be imported from a comma-separated values (CSV) file. The *SMS with Twilio* integration no longer requires you to add your SMS phone number to the setup page.

## 6 January 2021
{: #watson-assistant-jan062021}
{: release-note}

Import and export UI changes
:   The label on buttons for importing intents and entities changed from *Import* to *Upload*. The label on buttons for exporting intents and entities changed from *Export* to *Download*.

## 4 January 2021
{: #watson-assistant-jan042021}
{: release-note}

Dialog methods updates
:   Documentation and examples were added for the following supported dialog methods:

    - `JSONArray.addAll(JSONArray)`
    - `JSONArray.containsIgnoreCase(value)`
    - `String.equals(String)`
    - `String.equalsIgnoreCase(String)`

    For more information, see [Expression language methods](/docs/assistant?topic=assistant-dialog-methods){: external}.

## 17 December 2020
{: #watson-assistant-dec172020}
{: release-note}

Accessibility improvements
:   The product was updated to provide enhanced accessibility features.

## 14 December 2020
{: #watson-assistant-dec142020}
{: release-note}

Increased Phone and SMS with Twilio integrations availability
:   These beta SMS and voice capabilities are now available from service instances that are hosted in Seoul, Tokyo, London, and Sydney.

Improved JSON editor
:   The JSON editor in the dialog skill was updated. The editor now uses JSON syntax highlighting and allows you to expand and collapse objects.

Connect to agent from actions skill
:   The actions skill now supports transferring a customer to an agent from within an action step. For more information, see [Deciding what to do next](/docs/assistant?topic=assistant-actions#actions-what-next){: external}.

## 4 December 2020
{: #watson-assistant-dec042020}
{: release-note}

Introducing more service desk options for web chat
:   When you deploy your assistant by using the web chat integration, there are now reference implementations that you can use for the following service desks:

    - Twilio Flex
    - Genesys Cloud

    Alternatively, you can bring your own service desk by using the service desk extension starter kit.

    For more information, see [Adding service desk support](/docs/assistant?topic=assistant-deploy-web-chat#deploy-web-chat-haa){: external}.

Autolearning has been moved and improved
:   Go to the *Analytics>Autolearning* page to enable the feature and see visualizations that illustrate how autolearning impacts your assistant's performance over time. For more information, see [Empower your skill to learn automatically](/docs/assistant?topic=assistant-autolearn){: external}.

Search from actions skill
:   The actions skill now supports triggering a search that uses your associated search skill from within an action step. For more information, see [Deciding what to do next](/docs/assistant?topic=assistant-actions#actions-what-next){: external}.

System entities language support change
:   The new system entities are now used by all skills except Korean-language dialog skills. If you have a Korean skill that uses the older version of the system entities, update it. The legacy version will stop being supported for Korean skills in March 2021. For more information, see [Legacy system entities](/docs/assistant?topic=assistant-legacy-system-entities){: external}.

Disambiguation selection enhancement
:   When a customer chooses an option from a disambiguation list, the corresponding intent is submitted. With this latest release, a confidence score of 1.0 is assigned to the intent. Previously, the original confidence score of the option was used.

Skill import improvements
:   Importing of large skills from JSON data is now processed in the background. When you import a JSON file to create a skill, the new skill tile appears immediately. However, depending on the size of the skill, it might not be available for several minutes while the import is being processed. During this time, the skill cannot be opened for editing or added to an assistant, and the skill tile shows the text **Processing**.

## 23 November 2020
{: #watson-assistant-nov232020}
{: release-note}

Deploy your assistant to WhatsApp!
:   Make your assistant available through Whatsapp messaging so it can exchange messages with your customers where they are. This beta integration creates a connection between your assistant and WhatsApp by using Twilio as a provider. For more information, see [Integrating with WhatsApp](/docs/assistant?topic=assistant-deploy-whatsapp){: external}.

## 13 November 2020
{: #watson-assistant-nov132020}
{: release-note}

New coverage metric and enhanced intent detection model
:   The following features are available in service instances hosted in all data center locations except Dallas.

Introducing the coverage metric!
:   Want a quick way to see how your dialog is doing at responding to customer queries? Enable the new coverage metric to find out. The coverage metric measures the rate at which your dialog is confident that it can address a customer's request per message. For conversations that are not covered, you can review the logs to learn more about what the customer wanted. For the metric to work, you must design your dialog to include an *Anything else* node that is processed when no other dialog node intents are matched. For more information, see [Graphs and statistics](/docs/assistant?topic=assistant-logs-overview#logs-overview-graphs){: external}.

Try out the enhanced intent detection model
:   The new model, which is being offered as a beta feature in English-language dialog and actions skills, is faster and more accurate. It combines traditional machine learning, transfer learning, and deep learning techniques in a cohesive model that is highly responsive at run time. For more information, see [Improved intent recognition](/docs/assistant?topic=assistant-intent-detection){: external}.

## 3 November 2020
{: #watson-assistant-nov032020}
{: release-note}

Suggestions are now generally available
:   The Suggestions feature that is available for the web chat integration is generally available and is enabled by default when you create a new web chat integration. For more information, see [Showing more suggestions](/docs/assistant?topic=assistant-deploy-web-chat#deploy-web-chat-alternate){: external}.

New languages supported by the dialog analysis notebook
:   The *Dialog skill analysis notebook* was updated with language support for French, German, Spanish, Czech, Italian, and Portuguese. For more information, see [Analysis notebooks](/docs/assistant?topic=assistant-logs-resources#logs-resources-jupyter-logs){: external}.

Visit the learning center!
:   Click the **Learning center** link that is displayed in the header of the skill pages to find helpful product tours. The tours guide you through the steps to follow to complete a range of tasks, from adding your first intent to a dialog skill to enhancing the conversation in an actions skill. The **Additional resources** page has links to relevant documentation topics and how-to videos. You can search the resource link titles to find what you're looking for quickly.

## 29 October 2020
{: #watson-assistant-oct292020}
{: release-note}

System entity support changes
:   For English, Brazilian Portuguese, Czech, Dutch, French, German, Italian, and Spanish dialog skills only the new system entities API version is supported. For backward compatibility, both the `interpretation` and `metadata` attributes are included with the recognized entity object. The new system entity version is enabled automatically for dialog skills in the Arabic, Chinese, Korean, and Japanese languages. You can choose to use the legacy version of the system entities API by switching to it from the **Options>System Entities** page. This settings page is not displayed in English, Brazilian Portuguese, Czech, Dutch, French, German, Italian, and Spanish dialog skills because use of the legacy version of the API is no longer supported for those languages. For more information about the new system entities, see [System entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 28 October 2020
{: #watson-assistant-oct282020}
{: release-note}

Introducing the *actions skill*!
:   The actions skill is the latest step in the continuing evolution of {{site.data.keyword.conversationshort}} as a software as a service application. The actions skill is designed to make it simple enough for *anyone* to build a virtual assistant. We've removed the need to navigate between intents, entities, and dialog to create conversational flows. Building can all now be done in one simple and intuitive interface.

    The actions skill is available as a beta feature. For more information, see [Adding an actions skill](/docs/assistant?topic=assistant-skill-actions-add){: external}.

Web chat integration is created automatically
:   When you create a new assistant, a web chat integration is created for you automatically (in addition to the preview link integration, which was created previously). These integrations are added also to the assistant that is auto-generated (named *My first assistant*) when you create a new service instance. For more information, see [Integrating the web chat with your website](/docs/assistant?topic=assistant-deploy-web-chat){: external}.

Text messaging integration was renamed
:   The *Twilio messaging* integration was renamed to *SMS with Twilio*.

## 9 October 2020
{: #watson-assistant-oct092020}
{: release-note}

Search skill update
:   Support was added for a new version of the {{site.data.keyword.discoveryshort}} API which adds the following capabilities:

    - The search skill can now connect to existing Premium {{site.data.keyword.discoveryshort}} service instances.

    - When you connect to a Box, Sharepoint, or Web crawl data collection, the result content fields are automatically populated for you. The **Title** now uses the `title` field from the source document instead of the `extracted_metadata.title` field, which provides better results.

## 1 October 2020
{: #watson-assistant-oct012020}
{: release-note}

Introducing the *Phone* integration!
:   Your customers are calling; now your assistant can answer. Add a phone integration to enable your assistant to answer customer support calls. The integration connects to your existing Session Initiation Protocol (SIP) trunk, which routes incoming calls to your assistant. For more information, see [Integrating with phone](/docs/assistant?topic=assistant-deploy-phone){: external}.

Introducing the *Twilio messaging* integration!
:   Enable your assistant to receive and respond to questions that customers submit by using SMS text messaging. When you enable both new integrations, your assistant can send text messages to a customer in the context of an ongoing phone conversation. For more information, see [Integrating with Twilio messaging](/docs/assistant?topic=assistant-deploy-sms){: external}.

    The *Phone* and *Twilio messaging* integrations are available as beta features in {{site.data.keyword.conversationshort}} service instances that are hosted in Dallas, Frankfurt, and Washington, DC.

The web chat integration is added to new assistants automatically
:   Much like the *Preview link* integration, the *Web chat* integration now is added to the *My first assistant* assistant that is created for new users automatically.

## 24 September 2020
{: #watson-assistant-sep242020}
{: release-note}

Introducing the containment metric!
:   Want a quick way to see how often your assistant has to ask for help? Enable the new containment metric to find out. The containment metric measures the rate at which your assistant is able to address a customer's goal without human intervention. For conversations that are not contained, you can review the logs to understand what led customers to seek help outside of the assistant. For the metric to work, you must design your dialog to flag requests for additional support when they occur. For more information, see [Graphs and statistics](/docs/assistant?topic=assistant-logs-overview#logs-overview-graphs){: external}.

Chat transfer improvements
:   When you add the *Connect to human agent* response type to a dialog node, you can now define messages to show to your customers during the transfer, and can specify service desk agent routing preferences. For more information, see [Adding a *Connect to human agent* response type](/docs/assistant?topic=assistant-dialog-overview#dialog-overview-add-connect-to-human-agent){: external}.

## 22 September 2020
{: #watson-assistant-sep222020}
{: release-note}

New API version
:   The current v2 API version is now `2020-09-24`. In this version, the structure of the `search` response type has changed. The `results` property has been removed and replaced with two new properties:

    - `primary_results` property includes the search results that should be displayed in the initial response to a user query.
    - `additional_results` property includes search results that can be displayed if the user wants to see more.

    The search skill configuration determines how many search results are included in the `primary_results` and `additional_results` properties.

Search skill improvements
:   The following improvements were made to the search skill:

    - **Control the number of search results**: You can now customize the number of search results that are shown in a response from the search skill. For more information, see [Configure the search](/docs/assistant?topic=assistant-skill-search-add#skill-search-add-configure){: external}.

    - **FAQ extraction is available for web crawl data collections**: When you create a web crawl data collection type, you can now enable the FAQ extraction beta feature. FAQ extraction allows the {{site.data.keyword.discoveryshort}} service to identify question and answer pairs that it finds as it crawls the website. For more information, see [Create a data collection](/docs/assistant?topic=assistant-skill-search-add#skill-search-add-create-discovery-collection){: external}.

## 16 September 2020
{: #watson-assistant-sep162020}
{: release-note}

Search skill refinement change
:   The search refinement beta feature that was added in [June](#24jun2020) now is disabled by default. Enable the feature to refine the search results that are returned from the {{site.data.keyword.discoveryshort}} service. For more information, see [Configure the search](/docs/assistant?topic=assistant-skill-search-add#skill-search-add-configure){: external}.

## 25 August 2020
{: #watson-assistant-aug252020}
{: release-note}

Give the web chat integration a try!
:   You can now use the web chat integration with a Lite plan. Previously, the web chat was available to Plus or higher plans only. For more information, see [Integrating the web chat with your website](/docs/assistant?topic=assistant-deploy-web-chat){: external}.

## 12 August 2020
{: #watson-assistant-aug122020}
{: release-note}

v2 Logs API is available
:   If you have a Premium plan, you can use the v2 API `logs` method to list log events for an assistant. For more information, see the [API reference](https://cloud.ibm.com/apidocs/assistant/assistant-v2#listlogs){: external} documentation.

## 5 August 2020
{: #watson-assistant-aug052020}
{: release-note}

Enable your skill to improve itself
:   Try the new **autolearning** beta feature to empower your skill to improve itself automatically over time. Your skill observes customer choices to understand which choices are most often the best. As its confidence grows, your skill presents better options to get the right answers to your customers with fewer clicks. For more information, see [Empower your skill to learn over time](/docs/assistant?topic=assistant-autolearn){: external}.

Show more of search results
:   When search results are returned from the search skill, the customer can now click a twistie to expand the search result card to see more of the returned text.

## 29 July 2020
{: #watson-assistant-jul292020}
{: release-note}

The @sys-location and @sys-person system entities were removed
:   The `@sys-location` and `@sys-person` system entities are no longer listed on the *System entities* page. If your dialog uses one of these entities, a red `Entity not created` notification is displayed to inform you that the entity is not recognized.

Skill menu actions moved
:   The menu that was displayed in the header of the skill while you were working with a skill was removed. The actions that were available from the menu, such as import and export, are still available. Go to the Skills page, and click the menu on the skill tile.

    The import skill process was updated to support overwriting an existing skill on import. For more information, see [Overwriting a skill](/docs/assistant?topic=assistant-skill-tasks#skill-tasks-overwrite){: external}.

Dialog issues were addressed
:   These dialog issues were addressed:
    - Fixed an issue with adding a jump-to from a conditional response in one node to a conditional response in another node.
    - The page now responds better when you scroll horizontally to see multiple levels of child nodes.

## 15 July 2020
{: #watson-assistant-jul152020}
{: release-note}

Support ended for @sys-location and @sys-person
:   The person and location system entities, which were available as a beta feature in English dialog skills only, are no longer supported. You cannot enable them. If your dialog uses them, they are ignored by the service.

    Use contextual entities to teach your skill to recognize the context in which such names are used. For more information about contextual entities, see [Annotation-based method](/docs/assistant?topic=assistant-entities#entities-annotations-overview){: external}.

    For more information about how to use contextual entites to identify names of people, see the [Detecting Names And Locations With {{site.data.keyword.conversationshort}}](https://medium.com/ibm-watson/detecting-names-and-locations-with-watson-assistant-e3e1fa2a8427){: external} blog post on Medium.

How legacy numeric system entities are processed has changed
:   All new dialog skills use the new system entities automatically.

    For existing skills that use legacy numeric system entities, how the entities are processed now differs based on the skill language.

    - Arabic, Chinese, Korean, and Japanese dialog skills that use legacy numeric system entities function the same as before.
    - If you choose to continue to use the legacy system entities in European-language dialog skills, a new legacy API format is used. The new legacy API format simulates the legacy system entities behavior. In particular, it returns a `metadata` object and does not stop the service from idenfifying multiple system entities for the same input string. In addition, it returns an `interpretation` object, which was introduced with the new version of system entities. Review the `interpretation` object to see the useful information that is returned by the new version.

    Update your skills to use the new system entities from the **Options>System Entities** page.

Web chat security is generally available
:   Enable the security feature of web chat so that you can verify that messages sent to your assistant come from only your customers and can pass sensitive information to your assistant.

    When configuring the JWT, you no longer need to specify the Authentication Context Class Reference (acr) claim.

## 1 July 2020
{: #watson-assistant-jul012020}
{: release-note}

Salesforce support is generally available
:   Integrate your web chat with Salesforce so your assistant can transfer customers who asks to speak to a person to a Salesforce agent who can answer their questions. For more information, see [Integrating with Salesforce](/docs/assistant?topic=assistant-deploy-salesforce){: external}.

## 24 June 2020
{: #watson-assistant-jun242020}
{: release-note}

Getting intent recommendations from assistant logs is generally available
:   Use the chat log from one of your production assistants as the source for intent and intent user example recommendations. For more information, see [Getting help defining intents](/docs/assistant?topic=assistant-intent-recommendations){: external}.

Get better answers from search skill
:   The search skill now has a beta feature that limits the search results that are returned to include only those for which {{site.data.keyword.discoveryshort}} has calculated a 20% or higher confidence score. You can toggle the feature on or off from the *Refine results to return more selective answers* switch on the configuration page. You cannot change the confidence score threshold from 0.2. This beta feature is enabled by default. For more information, see [Creating a search skill](/docs/assistant?topic=assistant-skill-search-add){: external}.

## 3 June 2020
{: #watson-assistant-jun032020}
{: release-note}

Zendesk support is generally available
:   Integrate your web chat with Zendesk so your assistant can transfer customers who asks to speak to a person to a Zendesk agent who can answer their questions. And now you can secure the connection to Zendesk. For more information, see [Adding support for transfers](/docs/assistant?topic=assistant-deploy-zendesk){: external}.

Pricing plan changes
:   We continue to revamp the overall service plan structure for {{site.data.keyword.conversationshort}}. In April, we announced [a new low cost entry point](#watson-assistant-apr012020) for the Plus plan. Today, the Standard plan is being retired. Existing Standard plan users are not impacted; they can continue to work in their Standard instances. New users do not see the Standard plan as an option when they create a service instance. For more information, see the [Pricing](https://www.ibm.com/cloud/watson-assistant/pricing/){: external} page.

## 27 May 2020
{: #watson-assistant-may272020}
{: release-note}

Full language support for new system entities
:   The new version of the system entities is generally available in dialog skills of all languages, including Arabic, Chinese (Simplified), Chinese (Traditional), Korean, and Japanese. For more information, see [Supported languages](/docs/assistant?topic=assistant-language-support){: external}.

New system entities are enabled automatically
:   All new dialog skills use the new version of the system entities automatically. For more information, see [New system entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 22 May 2020
{: #watson-assistant-may222020}
{: release-note}

Spelling correction in v2 API
:   The v2 `message` API now supports spelling correction options. For more information see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v2#message){: external}.

## 21 May 2020
{: #watson-assistant-may212020}
{: release-note}

Preview link URL change
:   The URL for the preview link was changed. If you previously shared the link with teammates, provide them with the new URL.

## 15 May 2020
{: #watson-assistant-may152020}
{: release-note}

Private endpoints support is available in Plus plan
:   You can use private endpoints to route services over the {{site.data.keyword.cloud_notm}} private network instead of the public network. For more information, see [Private network endpoints](/docs/assistant?topic=assistant-security#security-private-endpoints){: external}. This feature was previously available to users of Premium plans only.

## 14 May 2020
{: #watson-assistant-may142020}
{: release-note}

Get skill owner information
:   The email address of the person who owns the service instance that you are using is displayed from the User account menu. This information is especially helpful if you want to contact the instance owner to request access changes. For more information about access control, see [Managing access to resources](/docs/assistant?topic=assistant-access-control){: external}.

System entity deprecation
:   As stated in the [March deprecation notice](#watson-assistant-mar012020), the `@sys-location` and `@sys-person` system entities that were available as a beta feature are deprecated. If you are using one of these system entities in your dialog, a toggle is displayed for the entity on the *System entities* page. You can [search your dialog](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-search){: external} to find out where you are currently using the entity, and remove it. Consider using a contextual entity to identify references to locations and people instead. After removing the entity from your dialog, disable the entity from the *System entities* page.

## 13 May 2020
{: #watson-assistant-may132020}
{: release-note}

Stateless v2 message API
:   The v2 runtime API now supports a new stateless `message` method. If you have a client application that manages its own state, you can use this new method to take advantage of [many of the benefits](https://medium.com/ibm-watson/the-new-watson-assistant-v2-stateless-api-unlock-enterprise-features-today-2c02a4bbdef5){: external} of the v2 API without the overhead of creating sessions. For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v2#message-stateless){: external}.

## 30 April 2020
{: #watson-assistant-apr302020}
{: release-note}

Web chat is generally available!
:   Add your assistant to your company website as a web chat widget that can help your customers with common questions and tasks. Service desk transfer support continues to be a beta feature. For more information, see [Integrating with your own website](/docs/assistant?topic=assistant-deploy-web-chat){: external}.

Secure your web chat
:   Enable the beta security feature of web chat so that you can verify that messages sent to your assistant come from only your customers and can pass sensitive information to your assistant.

## 27 April 2020
{: #watson-assistant-apr272020}
{: release-note}

Add personality to your assistant in web chat
:   You can add an assistant image to the web chat header to brand the window. You can add an avatar image that represents your assistant or a brand logo, for example. For more information, see [Integrating with your own web site](/docs/assistant?topic=assistant-deploy-web-chat){: external}.

Know your plan
:   Now your service plan is displayed in the page header. And if you have a Plus Trial plan, you can see how many days are left in the trial.

## 21 April 2020
{: #watson-assistant-apr212020}
{: release-note}

Fuzzy matching support was expanded
:   Added support for stemming and misspelling in French, German, and Czech dialog skills. This enhancement means that the assistant can recognize an entity value that is defined in its singular form but mentioned in its plural form in user input. It also can recognize conjugated forms of a verb that is specified as an entity value.

    For example, if your French-language dialog skill has an entity value of `animal`, it recognizes the plural form of the word (`animaux`) when it is mentioned in user input. If your German-language dialog skill has the root verb `haben` as an entity value, it recognizes conjugated forms of the verb (`hast`) in user input as mentions of the entity.

## 2 April 2020
{: #watson-assistant-apr022020}
{: release-note}

New and improved access control
:   Now, when you give other people access to your {{site.data.keyword.conversationshort}} resources, you have more control over the level of access they have to individual skills and assistants. You can give one person read-only access to a production skill and manager-level access to a development skill, for example. For more information, see [Managing access to resources](/docs/assistant?topic=assistant-access-control){: external}.

    Can't see Analytics anymore? If you cannot do things that you could do before, you might not have appropriate access. Ask the service instance owner to change your service access role. For more information, see [How to keep your access](/docs/assistant?topic=assistant-access-control#access-control-prep){: external}.

    If you can't access the API Details for a skill or assistant anymore, you might not have the access role that is required to use the instance-level API credentials. You can use a personal API key instead. For more information, see [Getting API information](/docs/assistant?topic=assistant-assistant-settings#assistant-settings-api-details){: external}.

## 1 April 2020
{: #watson-assistant-apr012020}
{: release-note}

Plus plan changes
:   The Plus plan is now available starting at $120/month for 1,000 users on pay-as-you-go or subscription IBM Cloud accounts. And you can subscribe without contacting Sales.

French language beta support added for contextual entities
:   You can add contextual entities to French-language dialog skills. For more information about contextual entities, see [Creating entities](/docs/assistant?topic=assistant-entities#entities-annotations-overview){: external}.

New API version
:   The current API version is now `2020-04-01`. The following change was made with this version:

    - An `integrations` property was added to the V2 `/message` context. The service now expects the `context.integrations` property to conform to a specific schema in which the allowed values are as follows:

        - `chat`
        - `facebook`
        - `intercom`
        - `liveengage`
        - `salesforce`
        - `slack`
        - `service_desk`
        - `text_messaging`
        - `voice_telephony`
        - `zendesk`

    If your app uses a `context.integrations` property that does not conform to the schema, a 400 error code will be returned.

## 31 March 2020
{: #watson-assistant-mar312020}
{: release-note}

The web chat integration was updated
:   The update adds an `isTrackingEnabled` parameter. You can add this parameter and set it to `false` to add the `X-Watson-Learning-Opt-Out` header to each `/message` request that originates from the web chat. For more information about the header, see [Data collection](https://cloud.ibm.com/apidocs/assistant/assistant-v2#data-collection){: external}. For more information about the parameter, see [Configuration](https://integrations.us-south.assistant.watson.cloud.ibm.com/web/developer-documentation/api-configuration){: external}.

## 26 March 2020
{: #watson-assistant-mar262020}
{: release-note}

The Covid-19 content catalog is available in Brazilian Portuguese, French, and Spanish
:   The content catalog defines a group of intents that recognize the common types of questions people ask about the novel coronavirus. You can use the catalog to jump-start development of chatbots that can answer questions about the virus and help to minimize the anxiety and misinformation associated with it. For more information about how to add a content catalog to your skill, see [Using content catalogs](/docs/assistant?topic=assistant-catalog){: external}.

## 19 March 2020
{: #watson-assistant-mar192020}
{: release-note}

A Covid-19 content catalog is available
:   The English-only content catalog defines a group of intents that recognize the common types of questions people ask about the novel coronavirus. The World Health Organization characterized COVID-19 as a pandemic on 11 March 2020. You can use the catalog to jump-start development of chatbots that can answer questions about the virus and help to minimize the anxiety and misinformation associated with it. For more information about how to add a content catalog to your skill, see [Using content catalogs](/docs/assistant?topic=assistant-catalog){: external}.

Fixed a problem with missing User Conversation data
:   A recent change resulted in no logs being shown in the User Conversations page unless you had a skill as the chosen data source. And the chosen skill had to be the same skill (with same skill ID) that was connected to the assistant when the user messages were submitted.

## 18 March 2020
{: #watson-assistant-mar182020}
{: release-note}

Technology preview is discontinued
:   The technology preview user interface was replaced with the {{site.data.keyword.conversationshort}} standard user interface. If you used an Actions page to create actions and steps for your skill previously, you cannot access the Actions page anymore. Instead, use the Intents and Dialog pages to work with your skill.

## 16 March 2020
{: #watson-assistant-mar162020}
{: release-note}

Instructions updated for Slack integrations
:   The steps required to set up a Slack integration have changed to reflect permission assignment changes that were made by Slack. For more information, see [Integrating with Slack](/docs/assistant?topic=assistant-deploy-slack){: external}.

Order of response types is preserved
:   Previously, if you included a response type of **Search skill** in a list of response types for a dialog node, the search results were displayed last despite its placement in the list. This behavior was changed to show the search results in the appropriate order, namely in the sequence in which the search skill response type is listed for the dialog node.

## 10 March 2020
{: #watson-assistant-mar102020}
{: release-note}

Contextual entity support is generally available
:   You can add contextual entities to English-language dialog skills. For more information about contextual entities, see [Creating entities](/docs/assistant?topic=assistant-entities#entities-annotations-overview){: external}.

French language support added for autocorrection
:   Autocorrection helps your assistant understand what your customers want. It corrects misspellings in the input that customers submit before the input is evaluated. With more precise input, your assistant can more easily recognize entity mentions and understand the customer's intent. See [Correcting user input](/docs/assistant?topic=assistant-dialog-runtime-spell-check){: external} for more details.

The new system entities are used by new skills
:   For new English, Brazilian Portuguese, Czech, Dutch, French, German, Italian, and Spanish dialog skills, the new system entities are enabled automatically. If you decide to turn on a system entity and add it to your dialog, it's the new and improved version of the system entity that is used. For more information, see [New system entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 6 March 2020
{: #watson-assistant-mar062020}
{: release-note}

Transfer a web chat conversation to a human agent
:   Delight your customers with 360-degree support by integrating your web chat with a third-party service desk solution. When a customer asks to speak to a person, you can connect them to an agent through a service desk solution, such as Zendesk or Salesforce. Service desk support is a beta feature. For more information, see [Adding support for transfers](/docs/assistant?topic=assistant-deploy-web-chat#deploy-web-chat-haa){: external}.

## 2 March 2020
{: #watson-assistant-mar022020}
{: release-note}

Known issue accessing logs
:   If you cannot access user logs from the Analytics page, ask the owner of the service instance for the skill to change your service level access to make you a Manager of the instance. For more information about access control, see [Managing access to resources](/docs/assistant?topic=assistant-access-control){: external}.

## 1 March 2020 deprecation notice
{: #watson-assistant-mar012020}
{: release-note}

March 2020 deprecation notice
:   To help us continue to improve and expand the capabilities of the assistants you build with {{site.data.keyword.conversationshort}}, we are deprecating some of the older technologies. Support for the older technologies will end in June 2020. Take action now to test and adopt the new technologies, so your skills and assistants will be ready when the old technologies stop being supported.

    The following technologies are being deprecated:

    - **Legacy version of numeric system entities**

        We released a whole new infrastructure for our numeric system entities across all languages except Chinese, Korean, Japanese and Arabic. The updated `@sys-number`, `@sys-date`, `@sys-time`, `@sys-currency`, and `@sys-percentage` entities provide superior number recognition with higher precision. For more information about the new system entities, see [System entity details](/docs/assistant?topic=assistant-system-entities){: external}.

        The old version of the numeric system entities will stop being supported in June 2020 for English, Brazilian Portuguese, Czech, Dutch, French, German, Italian, and Spanish dialog skills.

        ***Action***: In each dialog skill where you use numeric system entities, go to the **Options>System entities** page and turn on the new system entities. Take some time to test the new version of system entities with your own dialogs to make sure they continue to work as expected. As you adopt the new system entities, share your feedback about your experience with the new technology.

    - **Person and location system entities**

        The `@sys-person` and `@sys-location` system entities, which were available in English as a beta only, are being deprecated. Consider using contextual entities as a way to capture these types of proper nouns. Instead of trying to add a dictionary-based entity that covers every permutation of the names for people or cities, for example, you can teach your skill to recognize the context in which such names are used. For more information about contextual entities, see [Annotation-based method](/docs/assistant?topic=assistant-entities#entities-annotations-overview){: external}.

        ***Action***: Remove references to `@sys-person` and `@sys-location` from your dialogs. Turn off the `@sys-person` and `@sys-location` system entities to prevent yourself or others from adding them to a dialog inadvertently.

    - **Irrelevance detection**

        We revised the irrelevance detection classification algorithm to make it even smarter out of the box. Now, even before you begin to teach the system about irrelevant requests, it is able to recognize user input that your skill is not designed to address. For more information, see [Irrelevance detection](/docs/assistant?topic=assistant-irrelevance-detection){: external}.

        ***Action***: In each dialog skill, go to the **Options>Irrelevance detection** page and turn on the new classification model. Make sure everything works as well, if not better, than it did before. Share your feedback.

    - **Old API version dates**

        v1 API versions that are dated on or before `2017-02-03` are being deprecated. When you send calls to the service with earlier API version dates, they will receive properly formatted and valid responses for a time, so you can gracefully transition to using the later API versions. However, the confidence scores and other results that are sent in the response will reflect those generated by a more recent version of the API.

        ***Action***: Do some testing of calls with the latest version to verify that things work as expected. Some functionality has changed over the last few years. After testing, change the version date on any API calls that you make from your applications.

## 28 February 2020
{: #watson-assistant-feb282020}
{: release-note}

{{site.data.keyword.conversationfull}} is available in {{site.data.keyword.icp4dfull_notm}}
:   The service can be installed on-premises in environments where {{site.data.keyword.icp4dfull_notm}} 2.5 is installed on OpenShift or standalone. See the [{{site.data.keyword.icp4dfull_notm}} documentation](https://www.ibm.com/support/knowledgecenter/SSQNUZ_2.5.0/cpd/svc/watson/assistant-overview.html){: external} for more information.

## 26 February 2020
{: #watson-assistant-feb262020}
{: release-note}

Slot `Save it as` field retains your edits
:   When you edit what gets saved for a slot by using the JSON editor to edit the value of the context variable to be something other than what is specified in the **Check for** field, your changes are kept even if someone subsequently clicks the **Save it as** field.

## 20 February 2020
{: #watson-assistant-feb202020}
{: release-note}

Access control changes are coming
:   Notifications are displayed in the user interface for anyone with Reader and Writer level access to a service instance. The notification explains that access control is going to change soon, and that what they can do in the instance will change unless they are given Manager service access beforehand. For more information, see [Preventing loss of access](/docs/assistant?topic=assistant-access-control){: external}.

## 14 February 2020
{: #watson-assistant-feb142020}
{: release-note}

Get intent recommendations from an assistant log
:   You can now use the chat log from one of your production assistants as the source for intent and intent user example recommendations. See [Getting help defining intents](/docs/assistant?topic=assistant-intent-recommendations){: external}. This capability is a beta feature.

    With the introduction of this feature, how CSV log files are stored also changed. Previously, a log CSV file that you uploaded to one skill was shared by all of the skills in that service instance. Now, a CSV file that you upload to one skill is available for use only by that one skill. For existing instances with CSV files, the shared CSV files are available to each of the skills in the instance. You can delete a CSV file from a skill that doesn't use it by managing the recommendation sources for the skill.

More web chat color settings
:   You can now specify the color of more elements of the web chat integration. For example, you can define one color for the web chat window header. You can define a different color for the user message bubble. And another color for interactive components, such as the launcher button for the chat.

## 13 February 2020
{: #watson-assistant-feb132020}
{: release-note}

Track API events
:   Premium plan users can now use the Activity Tracker service to track how users and applications interact with {{site.data.keyword.conversationfull}} in {{site.data.keyword.cloud}}. See [Activity Tracker events](/docs/assistant?topic=assistant-at-events){: external}.

## 5 February 2020
{: #watson-assistant-feb052020}
{: release-note}

New API version
:   The current API version is now `2020-02-05`. The following changes were made with this version:

    - When a dialog node's response type is `connect-to-agent`, the node's `title` is used as the `topic` value. Previously, `user_label` was used.

    - The `alternate_intents` property is stored as a Boolean value instead of a String.

## 4 February 2020
{: #watson-assistant-feb042020}
{: release-note}

Product user interface makeover
:   The UI has been updated to be more intuitive, responsive, and consistent across its pages. While the look and feel of the UI elements has changed, their function has not.

Requesting early access
:   The button you click to request participation in the early access program has moved from the Skills page to the user account menu. For more information, see [Feedback](/docs/assistant?topic=assistant-feedback#feedback-beta){: external}.

## 24 January 2020
{: #watson-assistant-jan242020}
{: release-note}

New system entities are now generally available in multiple languages
:   The new and improved numeric system entities are now generally available in all supported languages, except Arabic, Chinese, Japanese, and Korean, where they are available as a beta feature. They are not used by your dialog skill unless you enable them from the **Options>System entities** page. For more information, see [New system entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 14 January 2020
{: #watson-assistant-jan142020}
{: release-note}

Fixed an error message that was displayed when opening an instance
:   An error that was displayed when you launched {{site.data.keyword.conversationshort}} from the {{site.data.keyword.cloud}} dashboard has been fixed. Previously, an error message that said, `Module 'ui-router' is not available! You either misspelled the module name or forgot to load it` would sometimes be displayed.

## 12 December 2019
{: #watson-assistant-dec122019}
{: release-note}

Support for private network endpoints
:   Users of Premium plans can create private network endpoints to connect to {{site.data.keyword.conversationshort}} over a private network. Connections to private network endpoints do not require public internet access. For more information, see [Protecting sensitive information](/docs/assistant?topic=assistant-security){: external}.

Full support for IBM Cloud IAM
:   {{site.data.keyword.conversationshort}} now supports the full implementation of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM). API keys for Watson services are no longer limited to a single service instance. You can create access policies and API keys that apply to more than one service, and you can grant access between services.

    - To support this change, the API service endpoints use a different domain and include the service instance ID. The pattern is `api.{location}.{offering}.watson.cloud.ibm.com/instances/{instance_id}`.

        Example URL for an instance hosted in the Dallas location: `api.us-south.assistant.watson.cloud.ibm.com/instances/6bbda3b3-d572-45e1-8c54-22d6ed9e52c2`

        The previous public endpoint domain was `watsonplatform.net`.

        For more information, see the [API reference](https://cloud.ibm.com/apidocs/assistant/assistant-v2#service-endpoint){: external}.

        These URLs do not introduce a breaking change. The new URLs work both for your existing service instances and for new instances. The original URLs continue to work on your existing service instances for at least one year (until December 2020).

    - For more information, see [Authenticating to Watson services](/docs/watson?topic=watson-iam){: external}.

## 26 November 2019
{: #watson-assistant-nov262019}
{: release-note}

Disambiguation is available to everyone
:   Disambiguation is now available to users of every plan type.

    The following changes were made to how it functions:

    - The text that you add to the dialog **node name** field now matters.

    - The text in the node name field might be shown to customers. The disambiguation feature shows it to customers if the assistant needs to ask them to clarify their meaning. The text you add as the node name must identify the purpose of the node clearly and succinctly, such as *Place an order* or *Get plan information*.

        If the *External node name* field exists and contains a summary of the node's purpose, then its summary is shown in the disambiguation list instead. Otherwise, the dialog node name content is shown.

      - Disambiguation is enabled automatically for all nodes. You can disable it for the entire dialog or for individual dialog nodes.

      - When testing, you might notice that the order of the options in the disambiguation list changes from one test run to the next. Don't worry; this new behavior is intended. As part of work being done to help the assistant learn automatically from user choices, the order of the options in the disambiguation list is being randomized on purpose. Changing the order helps to avoid bias that can be introduced by a percentage of people who always pick the first option without first reviewing their choices.

## 12 November 2019
{: #watson-assistant-nov122019}
{: release-note}

Slot prompt JSON editor
:   You can now use the context or JSON editors for the slot response field where you define the question that your assistant asks to get information it needs from the customer. For more information about slots, see [Gathering information with slots](/docs/assistant?topic=assistant-dialog-slots){: external}.

New South Korea location
:   You can now create {{site.data.keyword.conversationshort}} instances in the Seoul location. As with other locations, the {{site.data.keyword.cloud_notm}} Seoul location uses token-based Identity and Access Management (IAM) authentication.

Technology preview
:   A technology preview experience was released. A select set of new users are being presented with a new user interface that takes a different approach to building an assistant.

## 7 November 2019
{: #watson-assistant-nov072019}
{: release-note}

Irrelevance detection has been added
:   When enabled, a supplemental model is used to help identify utterances that are irrelevant and should not be answered by the dialog skill. This new model is especially beneficial for skills that have not been trained on what subjects to ignore. This feature is available for English skills only. For more information, see [Irrelevance detection](/docs/assistant?topic=assistant-irrelevance-detection){: external}.

Time zone support for now() method
:   You can now specify the time zone for the date and time that is returned by the `now()` method. See [Now()](/docs/assistant?topic=assistant-dialog-methods#dialog-methods-dates-now){: external}.

## 24 October 2019
{: #watson-assistant-oct242019}
{: release-note}

Testing improvement
:   You can now see the top three intents that were recognized in a test user input from the "Try it out" pane. For more details, see [Testing your dialog](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-test){: external}.

Error message when opening an instance
:   When you launch {{site.data.keyword.conversationshort}} from the {{site.data.keyword.cloud}} dashboard, you might see an error message that says, `Module 'ui-router' is not available! You either misspelled the module name or forgot to load it.` You can ignore the message. Refresh the web browser page to close the notification.

## 16 October 2019
{: #watson-assistant-oct162019}
{: release-note}

The changes from 14 October are now available in Dallas.

## 14 October 2019
{: #watson-assistant-oct142019}
{: release-note}

Deploy your assistant in minutes
:   Create a web chat integration to embed your assistant into a page on your website as a chat widget. See [Integrating with your own website](/docs/assistant?topic=assistant-deploy-web-chat){: external}.

UI changes
:   The main menu options of **Assistants** and **Skills** have moved from being displayed in the page header to being shown as icons on the side of the page. The tabbed pages for the tools you use to develop a dialog skill were moved to a secondary navigation bar that is displayed when you open the skill.

Rich response types are supported in a dialog node with slots
:   You can display a list of options for a user to choose from as the prompt for a slot, for example.

Change to switching service instances
:   Where you go to switch service instances has changed. See [Switching the service instance](/docs/assistant?topic=assistant-assistant-settings#assistant-settings-switch-instance){: external}.

Known issue: Cannot rename search skills
:   You currently cannot rename a search skill after you create it.

## 9 October 2019
{: #watson-assistant-oct092019}
{: release-note}

New system entities changes
:   The following updates have been made:

    - In addition to English and German, the new numeric system entities are now available in these languages: Brazilian Portuguese, Czech, French, Italian, and Spanish.

    - The `part_of_day` property of the `@sys-time` entity now returns a time range instead of a single time value.

## 23 September 2019
{: #watson-assistant-sep232019}
{: release-note}

Dallas updates
:   The updates from 20 September are now available to service instances hosted in Dallas.

## 20 September 2019
{: #watson-assistant-sep202019}
{: release-note}

Inactivity timeout increase
:   The maximum inactivity timeout can now be extended to up to 7 days for Premium plans. See [Changing the inactivity timeout setting](/docs/assistant?topic=assistant-assistant-settings){: external}.

Pattern entity fix
:   A change that was introduced in the previous release which changed all alphabetic characters to lowercase at the time an entity value was added has been fixed. The case of any alphabetic characters that are part of a pattern entity value are no longer changed when the value is added.

Dialog text response syntax fix
:   Fixed a bug in which the format of a dialog response reverted to an earlier version of the JSON syntax. Standard text responses were being saved as `output.text` instead of `output.generic`. For more information about the `output` object, see [Anatomy of a dialog call](/docs/assistant?topic=assistant-dialog-runtime-context){: external}.

## 13 September 2019
{: #watson-assistant-sep132019}
{: release-note}

Improved Entities and Intents page responsiveness
:   The Entities and Intents pages were updated to use a new JavaScript library that increases the page responsiveness. As a result, the look of some graphical user interface elements, such as buttons, changed slightly, but the function did not.

Creating contextual entities got easier
:   The process you use to annotate entity mentions from intent user examples was improved. You can now put the intent page into annotation mode to more easily select and label mentions. See [Adding contextual entities](/docs/assistant?topic=assistant-entities#entities-create-annotation-based){: external}.

## 6 September 2019
{: #watson-assistant-sep062019}
{: release-note}

Label character limit increase
:   The limit to the number of characters allowed for a label that you define for an option response type changed from 64 characters to 2,048 characters.

## 12 August 2019
{: #watson-assistant-aug122019}
{: release-note}

New dialog method
:   The `getMatch` method was added. You can use this method to extract a specific occurrence of a regular expression pattern that recurs in user input. For more details, see the [dialog methods](/docs/assistant?topic=assistant-dialog-methods#dialog-methods-strings-getMatch){: external} topic.

## 9 August 2019
{: #watson-assistant-aug092019}
{: release-note}

Introductory product tour
:   For some first-time users, a new introductory product tour is shown that the user can choose to follow to perform the initial steps of creating an assistant.

## 6 August 2019
{: #watson-assistant-aug062019}
{: release-note}

- Webhook callouts and Dialog page improvements are available in Dallas.

## 1 August 2019
{: #watson-assistant-aug012019}
{: release-note}

Webhook callouts are available
:   Add webhooks to dialog nodes to make programmatic calls to an external application as part of the conversational flow. The new Webhook support simplifies the callout implementation process. (No more `action` JSON objects required.) For more information, see [Making a programmatic call from a dialog node](/docs/assistant?topic=assistant-dialog-webhooks){: external}.

Improved dialog page responsiveness
:   In all service instances, the user interface of the Dialog page was updated to use a new JavaScript library that increases the page responsiveness. As a result, the look of some graphical user interface elements, such as buttons, changed slightly, but the function did not.

## 31 July 2019
{: #watson-assistant-jul312019}
{: release-note}

Search skill and autocorrection are generally available
:   The search skill and spelling autocorrection features, which were previously available as beta features, are now generally available.

    - Search skills can be created by users of Plus or Premium plans only.

    - You can enable autocorrection for English-language dialog skills only. It is enabled automatically for new English-language dialog skills.

## 26 July 2019
{: #watson-assistant-jul262019}
{: release-note}

Missing skills issue is resolved
:   In some cases, workspaces that were created through the API only were not being displayed when you opened the {{site.data.keyword.conversationshort}} user interface. This issue has been addressed. All workspaces that you create by using the API are displayed as dialog skills when you open the user interface.

## 23 July 2019
{: #watson-assistant-ju23l2019}
{: release-note}

Dialog search is fixed
:   In some skills, the search function was not working in the Dialog page. The issue is now fixed.

## 17 July 2019
{: #watson-assistant-jul172019}
{: release-note}

Disambiguation choice limit
:   You can now set the maximum number of options to show to users when the assistant asks them to clarify what they want to do. For more information about disambiguation, see [Disambiguation](/docs/assistant?topic=assistant-dialog-runtime#dialog-runtime-disambiguation){: external}.

Dialog search issue
:   In some skills, the search function is not working in the Dialog page. A new user interface library, which increases the page responsiveness, is being rolled out to existing service instances in phases. This search issue affects only dialog skills for which the new library is not yet enabled.

Missing skills issue
:   In some cases, workspaces that were created through the API only are not being displayed when you open the {{site.data.keyword.conversationshort}} user interface. Normally, these workspaces are displayed as dialog skills. If you do not see your skills from the UI, don't worry; they are not gone. Contact support to report the issue, so the team can enable the workspaces to be displayed properly.

## 15 July 2019
{: #watson-assistant-jul152019}
{: release-note}

Numeric system entities upgrade available in Dallas
:   The new system entities are now also available as a beta feature for instances that are hosted in Dallas. See [New system entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 12 June 2019
{: #watson-assistant-jun122019}
{: release-note}

Numeric system entities upgrade
:   New system entities are available as a beta feature that you can enable in dialog skills that are written in English or German. The revised system entities offer better date and time understanding. They can recognize date and number spans, national holiday references, and classify mentions with more precision. For example, a date such as `May 15` is recognized as a date mention(`@sys-date:2019-05-15`), and is *not* also identified as a number mention (`@sys-number:15`). See [New system entities](/docs/assistant?topic=assistant-system-entities){: external}.

A Plus Trial plan is available
:   You can use the free Plus Trial plan to try out the features of the Plus plan as you make a purchasing decision. The trial lasts for 30 days. After the trial period ends, if you do not upgrade to a Plus plan, your Plus Trial instance is converted to a Lite plan instance.

## 23 May 2019
{: #watson-assistant-may232019}
{: release-note}

Updated navigation
:   The home page was removed, and the order of the Assistants and Skills tabs was reversed. The new tab order encourages you to start your development work by creating an assistant, and then a skill.

Disambiguation settings have moved
:   The toggle to enable disamibugation, which is a feature that is available to Plus and Premium plan users only, has moved. The **Settings** button was removed from the **Dialog** page. You can now enable disambiguation and configure it from the skill's **Options** tab.

An introductory tour is now available
:   A short product tour is now displayed when a new service instance is created. Brand new users are also given help as they start development. A new assistant is created for them automatically. Informational popups are displayed to introduce the product user interface features, and guide the new user toward taking the key first step of creating a dialog skill.

## 10 April 2019
{: #watson-assistant-apr102019}
{: release-note}

Autocorrection is now available
:   Autocorrection is a beta feature that helps your assistant understand what your customers want. It corrects misspellings in the input that customers submit before the input is evaluated. With more precise input, your assistant can more easily recognize entity mentions and understand the customer's intent. See [Correcting user input](/docs/assistant?topic=assistant-dialog-runtime-spell-check){: external} for more details.

## 22 March 2019
{: #watson-assistant-mar222019}
{: release-note}

Introducing search skill
:   A search skill helps you to make your assistant useful to customers faster. Customer inquiries that you did not anticipate and so have not built dialog logic to handle can be met with useful responses. Instead of saying it can't help, the assistant can query an external data source to find relevant information to share in its response. Over time, you can build dialog responses to answer customer queries that require follow-up questions to clarify the user's meaning or for which a short and clear response is suitable. And you can use search skill responses to address more open-ended customer queries that require a longer explanation. This beta feature is available to users of Premium and Plus service plans only.

    See [Building a search skill](/docs/assistant?topic=assistant-skill-search-add){: external} for more details.

## 14 March 2019
{: #watson-assistant-mar142019}
{: release-note}

Have Watson help you build intents
:   Use Watson machine learning technology to help you choose the right intents for your assistant. Watson analyzes your existing call center log data to identify the customer questions and requests that occur most often. It then recommends intents and user examples you can use to train your assistant so it can recognize the same and similar requests in future. Once you determine the right intents to use, you can augment them and keep them up-to-date over time using the intent user example recommendations functionality, which is already available. For more information, see [Get help defining intents](/docs/assistant?topic=assistant-intent-recommendations){: external}.

## 4 March 2019
{: #watson-assistant-mar042019}
{: release-note}

Simplified navigation
:   The sidebar navigation with separate *Build*,  *Improve*, and *Deploy* tabs has been removed. Now, you can get to all the tools you need to build a dialog skill from the main skill page.

Improve page is now called Analytics
:   The informational metrics that Watson generates from conversations between your users and your assistant moved from the *Improve* tab of the sidebar to a new tab on the main skill page called **Analytics**.

## 1 March 2019
{: #watson-assistant-mar012019}
{: release-note}

Japanese intent user example recommendations
:   You can now upload a file that contains raw user inputs in Japanese, such as user inquiries from a call center log, that Watson can analyze and mine for intent user example candidates. See [Adding examples from log files](/docs/assistant?topic=assistant-intent-recommendations){: external}.

## 28 February 2019
{: #watson-assistant-feb282019}
{: release-note}

New API version
:   The current API version is now `2019-02-28`. The following changes were made with this version:

    - The order in which conditions are evaluated in nodes with slots has changed. Previously, if you had a node with slots that allowed for digressions away, the `anything_else` root node was triggered before any of the slot level Not found conditions could be evaluated. The order of operations has been changed to address this behavior. Now, when a user digresses away from a node with slots, all the root nodes except the `anything_else` node are processed. Next, the slot level Not found conditions are evaluated. And, finally, the root level `anything_else` node is processed. To better understand the full order of operations for a node with slots, see [Slot usage tips](/docs/assistant?topic=assistant-dialog-slots#dialog-slots-node-level-handler){: external}.

    - Strings that begin with a number sign (#) in the `context` or `output` objects of a message are no longer treated as intent references.

      Previously, these strings were treated as intents automatically. For example, if you specified a context variable, such as `"color":"#FFFFFF"`, then the hex color code (#FFFFFF) would be treated as an intent. Your assistant would check whether an intent named #FFFFFF was detected in the user's input, and if not, would replace #FFFFFF with `false`. This replacement no longer occurs.

      Similarly, if you included a number sign (#) in the text string in a node response, you used to have to escape it by preceding it with a back slash (`\`). For example, `We are the \#1 seller of lobster rolls in Maine.` You no longer need to escape the `#` symbol in a text response.

      This change does not apply to node or condtional response conditions. Any strings that begin with a number sign (#) which are specified in conditions continue to be treated as intent references. Also, you can use SpEL expression syntax to force the system to treat a string in the `context` or `output` objects of a message as an intent. For example, specify the intent as `<? #intent-name ?>`.

## 25 February 2019
{: #watson-assistant-feb252019}
{: release-note}

Slack integration enhancement
:   You can now choose the type of event that triggers your assistant in a Slack channel. Previously, when you integrated your assistant with Slack, the assistant interacted with users through a direct message channel. Now, you can configure the assistant to listen for mentions, and respond when it is mentioned in other channels. You can choose to use one or both event types as the mechanism through which your assistant interacts with users.

## 11 February 2019
{: #watson-assistant-feb112019}
{: release-note}

Integrate with Intercom
:   Intercom, a leading customer service messaging platform, has partnered with IBM to add a new agent to the team, a virtual {{site.data.keyword.conversationshort}}. You can integrate your assistant with an Intercom application to enable the app to seamlessly pass user conversations between your assistant and human support agents. This integration is available to Plus and Premium plan users only. See [Integrating with Intercom](/docs/assistant?topic=assistant-deploy-intercom){: external} for more details.

## 8 February 2019
{: #watson-assistant-feb082019}
{: release-note}

Version your skills
:   You can now capture a snapshot of the the intents, entities, dialog, and configuration settings for a skill at key points during the development process. With versions, it's safe to get creative. You can deploy new design approaches in a test environment to validate them before you apply any updates to a production deployment of your assistant. See [Creating skill versions](/docs/assistant?topic=assistant-versions){: external} for more details.

Arabic content catalog
:   Users of Arabic-language skills can now add prebuilt intents to their dialogs. See [Using content catalogs](/docs/assistant?topic=assistant-catalog){: external} for more information.

## 17 January 2019
{: #watson-assistant-jan172019}
{: release-note}

Czech language support is generally available
:   Support for the Czech language is no longer classified as beta; it is now generally available. See [Supported languages](/docs/assistant?topic=assistant-language-support){: external} for more information.

Language support improvements
:   The language understanding components were updated to improve the following features:

    - German and Korean system entities

    - Intent classification tokenization for Arabic, Dutch, French, Italian, Japanese, Portuguese, and Spanish

## 4 January 2019
{: #watson-assistant-jan042019}
{: release-note}

IBM Cloud Functions in DC and London locations
:   You can now make programmatic calls to IBM Cloud Functions from the dialog of an assistant in a service instance that is hosted in the London and Washington, DC data centers. See [Making programmatic calls from a dialog node](/docs/assistant?topic=assistant-dialog-actions-client){: external}.

New methods for working with arrays
:   The following SpEL expression methods are available that make it easier to work with array values in your dialog:

    - **JSONArray.filter**: Filters an array by comparing each value in the array to a value that can vary based on user input.
    - **JSONArray.includesIntent**: Checks whether an `intents` array contains a particular intent.
    - **JSONArray.indexOf**: Gets the index number of a specific value in an array.
    - **JSONArray.joinToArray**: Applies formatting to values that are returned from an array.

   See the [array method documentation](/docs/assistant?topic=assistant-dialog-methods#dialog-methods-arrays){: external} for more details.

## 13 December 2018
{: #watson-assistant-dec132018}
{: release-note}

London data center
:   You can now create {{site.data.keyword.conversationshort}} service instances that are hosted in the London data center without syndication. See [Data centers](/docs/assistant?topic=assistant-services-information#services-information-regions){: external} for more details.

Dialog node limit changes
:   The dialog node limit was temporarily changed from 100,000 to 500 for new Standard plan instances. This limit change was later reversed. If you created a Standard plan instance during the time frame in which the limit was in effect, your dialogs might be impacted. The limit was in effect for skills created between 10 December and 12 December 2018. The lower limits will be removed from all impacted instances in January. If you need to have the lower limit lifted before then, open a support ticket.

## 1 December 2018
{: #watson-assistant-dec012018}
{: release-note}

Determine the number of dialog nodes
:   To determine the number of dialog nodes in a dialog skill, do one of the following things:

     - From the tool, if it is not associated with an assistant already, add the dialog skill to an assistant, and then view the skill tile from the main page of the assistant. The *trained data* section lists the number of dialog nodes.

     - Send a GET request to the /dialog_nodes API endpoint, and include the `include_count=true` parameter. For example:

        ```curl
        curl -u "apikey:{apikey}" "https://{service-hostname}/assistant/api/v1/workspaces/{workspace_id}/dialog_nodes?version=2018-09-20&include_count=true"
        ```
        {: codeblock}

        where {service-hostname} is the appropriate URL for your instance. For more details, see [Service endpoint](https://cloud.ibm.com/apidocs/assistant/assistant-v1#service-endpoint){: external}.

        In the response, the `total` attribute in the `pagination` object contains the number of dialog nodes.

        See [Troubleshooting skill import issues](/docs/assistant?topic=assistant-skill-dialog-add#skill-dialog-add-import-errors){: external} for information about how to edit skills that you want to continue using.

## 27 November 2018
{: #watson-assistant-nov272018}
{: release-note}

A new service plan, the Plus plan, is available
:   The new plan offers premium-level features at a lower price point. Unlike previous plans, the Plus plan is a user-based billing plan. It measures usage by the number of unique users that interact with your assistant over a given time period. To get the most from the plan, if you build your own client application, design your app such that it defines a unique ID for each user, and passes the user ID with each /message API call. For the built-in integrations, the session ID is used to identify user interactions with the assistant. See [User-based plans](/docs/assistant?topic=assistant-services-information#services-information-user-based-plans){: external} for more information.

    | Artifact | Limit |
    | --- | --- |
    | Assistants | 100 |
    | Contextual entities | 20 |
    | Contextual entity annotations | 2,000 |
    | Dialog nodes | 100,000 |
    | Entities | 1,000 |
    | Entity synonyms | 100,000 |
    | Entity values | 100,000 |
    | Intents | 2,000 |
    | Intent user examples | 25,000 |
    | Integrations | 100 |
    | Logs | 30 days |
    | Skills | 50 |
    {: caption="Plus plan limits" caption-side="top"}

User-based Premium plan
:   The Premium plan now bases its billing on the number of active unique users. If you choose to use this plan, design any custom applications that you build to properly identify the users who generate /message API calls. See [User-based plans](/docs/assistant?topic=assistant-services-information#services-information-user-based-plans){: external} for more information.

    Existing Premium plan service instances are not impacted by this change; they continue to use API-based billing methods. Only existing Premium plan users will see the API-based plan listed as the *Premium (API)* plan option.

    See {{site.data.keyword.conversationshort}} [service plan options](https://www.ibm.com/cloud/watson-assistant/pricing/){: external} for more information about all available service plans.

Intent user example recommendations
:   You can upload a file that contains raw user inputs, such as user inquiries from a call center log, that Watson can analyze and mine for intent user example candidates. See [Adding examples from log files](/docs/assistant?topic=assistant-intent-recommendations#intent-recommendations-get-example-recommendations-task){: external}.

## 20 November 2018
{: #watson-assistant-nov202018}
{: release-note}

**Recommendations are discontinued
:   The Recomendations section on the Improve tab was removed. Recommendations was a beta feature available to Premium plan users only. It recommended actions that users could take to improve their training data. Instead of consolidating recommendations in one place, recommendations are now being made available from the parts of the tool where you make actual training data changes. For example, while adding entity synonyms, you can now opt to see a list of synonymous terms that are recommended by Watson. If you are looking for other ways to analyze your user conversation logs in more detail, consider using Jupyter notebooks. See [Advanced tasks](/docs/assistant?topic=assistant-logs-resources){: external} for more details.

## 9 November 2018
{: #watson-assistant-nov092018}
{: release-note}

Major user interface revision
:   The {{site.data.keyword.conversationshort}} service has a new look and added features.

    This version of the tool was evaluated by beta program participants over the past several months.

    - **Skills**: What you think of as a *workspace* is now called a *skill*. A *dialog skill* is a container for the natural language processing training data and artifacts that enable your assistant to understand user questions, and respond to them.

    **Where are my workspaces?** Any workspaces that you created previously are now listed in your service instance as skills. Click the **Skills** tab to see them. For more information, see [Adding skills to your assistant](/docs/assistant?topic=assistant-skill-add){: external}.

    - **Assistants**: You can now publish your skill in just two steps. Add your skill to an assistant, and then set up one or more integrations with which to deploy your skill. The assistant adds a layer of function to your skill that enables {{site.data.keyword.conversationshort}} to orchestrate and manage the flow of information for you. See [Assistants](/docs/assistant?topic=assistant-assistants){: external}.

    - **Built-in integrations**: Instead of going to the **Deploy** tab to deploy your workspace, you add your dialog skill to an assistant, and add integrations to the assistant through which the skill is made available to your users. You do not need to build a custom front-end application and manage the conversation state from one call to the next. However, you can still do so if you want to. See [Adding integrations](/docs/assistant?topic=assistant-deploy-integration-add){: external} for more information.

    - **New major API version**: A V2 version of the API is available. This version provides access to methods you can use to interact with an assistant at run time. No more passing context with each API call; the session state is managed for you as part of the assistant layer.

    What is presented in the tooling as a dialog skill is effectively a wrapper for a V1 workspace. There are currently no API methods for authoring skills and assistants with the V2 API. However, you can continue to use the V1 API for authoring workspaces. See [API Overview](/docs/assistant?topic=assistant-api-overview){: external} for more details.

    - **Switching data sources**: It is now easier to improve the model in one skill with user conversation logs from a different skill. You do not need to rely on deployment IDs, but can simply pick the name of the assistant to which a skill was added and deployed to use its data. See [Improving across assistants](/docs/assistant?topic=assistant-logs#logs-deploy-id){: external}.

    - **Preview links from London instances**: If your service instance is hosted in London, then you must edit the preview link URL. The URL includes a region code for the region where the instance is hosted. Because instances in London are syndicated to Dallas, you must replace the `eu-gb` reference in the URL with `us-south` for the preview web page to render properly.

## 8 November 2018
{: #watson-assistant-nov082018}
{: release-note}

Japanese data center
:   You can now create {{site.data.keyword.conversationshort}} service instances that are hosted in the Tokyo data center. See [Data centers](/docs/assistant?topic=assistant-services-information#services-information-regions){: external} for more details.

## 30 October 2018
{: #watson-assistant-oct302018}
{: release-note}

New API authentication process
:   The {{site.data.keyword.conversationshort}} service transitioned from using Cloud Foundry to using token-based Identity and Access Management (IAM) authentication in the following regions:

    - Dallas (us-south)
    - Frankfurt (eu-de)

    For new service instances, you use IAM for authentication. You can pass either a bearer token or an API key. Tokens support authenticated requests without embedding service credentials in every call. API keys use basic authentication.

    For all existing service instances, you continue to use service credentials (`{username}:{password}`) for authentication.

## 25 October 2018
{: #watson-assistant-oct252018}
{: release-note}

Entity synonym recommendations are available in more languages
:   Synonym recommendation support was added for the French, Japanese, and Spanish languages.

## 26 September 2018
{: #watson-assistant-sep262018}
{: release-note}

{{site.data.keyword.conversationfull}} is available in {{site.data.keyword.icpfull}}
:   {{site.data.keyword.conversationfull}} is available in {{site.data.keyword.icpfull}}

## 21 September 2018
{: #watson-assistant-sep212018}
{: release-note}

New API version
:   The current API version is now `2018-09-20`. In this version, the `errors[].path` attribute of the error object that is returned by the API is expressed as a [JSON Pointer](https://tools.ietf.org/html/rfc6901){: external} instead of in dot notation form.

Web actions support
:   You can now call {{site.data.keyword.openwhisk_short}} web actions from a dialog node. See [Making programmatic calls from a dialog node](/docs/assistant?topic=assistant-dialog-actions-client){: external} for more details.

## 15 August 2018
{: #watson-assistant-aug152018}
{: release-note}

Entity fuzzy matching support improvements
:   Fuzzy matching is fully supported for English entities, and the misspelling feature is no longer a Beta-only feature for many other languages. See [Supported languages](/docs/assistant?topic=assistant-language-support){: external} for details.

## 6 August 2018
{: #watson-assistant-aug062018}
{: release-note}

Intent conflict resolution
:   The tool can now help you to resolve conflicts when two or more user examples in separate intents are similar to one another. Non-distinct user examples can weaken the training data and make it harder for your assistant to map user input to the appropriate intent at run time. See [Resolving intent conflicts](/docs/assistant?topic=assistant-intents#intents-resolve-conflicts){: external} for details.

Disambiguation
:   Enable disambiguation to allow your assistant to ask the user for help when it needs to decide between two or more viable dialog nodes to process for a response. See [Disambiguation](/docs/assistant?topic=assistant-dialog-runtime#dialog-runtime-disambiguation){: external} for more details.

Jump-to fix
:   Fixed a bug in the Dialogs tool which prevented you from being able to configure a jump-to that targets the response of a node with the `anything_else` special condition.

Digression return message
:   You can now specify text to display when the user returns to a node after a digression. The user will have seen the prompt for the node already. You can change the message slightly to let users know they are returning to where they left off. For example, specify a response like, `Where were we? Oh, yes...` See [Digressions](/docs/assistant?topic=assistant-dialog-runtime#dialog-runtime-digressions){: external} for more details.

## 12 July 2018
{: #watson-assistant-jul122018}
{: release-note}

Rich response types
:   You can now add rich responses that include elements such as images or buttons in addition to text, to your dialog. See [Rich responses](/docs/assistant?topic=assistant-dialog-overview#dialog-overview-multimedia){: external} for more information.

Contextual entities (Beta)
:   Contextual entities are entities that you define by labeling mentions of the entity type that occur in intent user examples. These entity types teach your assistant not only terms of interest, but also the context in which terms of interest typically appear in user utterances, enabling your assistant to recognize never-seen-before entity mentions based solely on how they are referenced in user input. For example, if you annotate the intent user example, `I want a flight to Boston` by labeling `Boston` as a `@destination` entity, then your assistant can recognize `Chicago` as a `@destination` mention in a user input that says, `I want a flight to Chicago.` This feature is currently available for English only. See [Adding contextual entities](/docs/assistant?topic=assistant-entities#entities-create-annotation-based){: external} for more information.

    When you access the tool with an Internet Explorer web browser, you cannot label entity mentions in intent user examples nor edit user example text.

Entity recommendations
:   Watson can now recommend synonyms for your entity values. The recommender finds related synonyms based on contextual similarity extracted from a vast body of existing information, including large sources of written text, and uses natural language processing techniques to identify words similar to the existing synonyms in your entity value. For more information see [Synonyms](/docs/assistant?topic=assistant-entities#entities-create-dictionary-based){: external}.

New API version
:   The current API version is now `2018-07-10`. This version introduces the following changes:

    - The content of the /message `output` object changed from being a `text` JSON object to being a `generic` array that supports multiple rich response types, including `image`, `option`, `pause`, and `text`.
    - Support for contextual entities was added.
    - You can no longer add user-defined properties in `context.metadata`. However, you can add them directly to `context`.

Overview page date filter
:   Use the new date filters to choose the period for which data is displayed. These filters affect all data shown on the page: not just the number of conversations displayed in the graph, but also the statistics displayed along with the graph, and the lists of top intents and entities. See [Controls](/docs/assistant?topic=assistant-logs-overview#logs-overview-controls){: external} for more information.

Pattern limit expanded
:   When using the **Patterns** field to [define specific patterns for an entity value](/docs/assistant?topic=assistant-entities#entities-patterns){: external}, the pattern (regular expression) is now limited to 512 characters.

## 2 July 2018
{: #watson-assistant-jul022018}
{: release-note}

Jump-tos from conditional responses
:   You can now configure a conditional response to jump directly to another node. See [Conditional responses](/docs/assistant?topic=assistant-dialog-overview#dialog-overview-multiple){: external} for more details.

## 21 June 2018
{: #watson-assistant-jun212018}
{: release-note}

Language updates for system entities
:   Dutch and Simplified Chinese language support are now generally available. Dutch language support includes fuzzy matching for misspellings. Traditional Chinese language support includes the availability of [system entities](/docs/assistant?topic=assistant-system-entities){: external} in beta release. See [Supported languages](/docs/assistant?topic=assistant-language-support){: external} for details.

## 14 June 2018
{: #watson-assistant-jun142018}
{: release-note}

Washington, DC data center opens
:   You can now create {{site.data.keyword.conversationshort}} service instances that are hosted in the Washington, DC data center. See [Data centers](/docs/assistant?topic=assistant-services-information#services-information-regions){: external} for more details.

New API authentication process
:   The {{site.data.keyword.conversationshort}} service has a new API authentication process for service instances that are hosted in the following regions:

    - Washington, DC (us-east) as of 14 June 2018
    - Sydney, Australia (au-syd) as of 7 May 2018

    {{site.data.keyword.cloud}} is migrating to token-based Identity and Access Management (IAM) authentication.

    For new service instances in the regions listed, you use IAM for authentication. You can pass either a bearer token or an API key. Tokens support authenticated requests without embedding service credentials in every call. API keys use basic authentication.

    For all new and existing service instances in other regions, you continue to use service credentials (`{username}:{password}`) for authentication.

    When you use any of the Watson SDKs, you can pass the API key and let the SDK manage the lifecycle of the tokens. For more information and examples, see [Authentication](https://cloud.ibm.com/apidocs/assistant/assistant-v2#authentication){: external} in the API reference.

    If you are not sure which type of authentication to use, view the {{site.data.keyword.conversationshort}} credentials by clicking the service instance from the Services section of the [{{site.data.keyword.Bluemix_notm}} Resource List](https://cloud.ibm.com){: external}.

## 25 May 2018
{: #watson-assistant-may252018}
{: release-note}

New sample workspace
:   The sample workspace that is provided for you to explore or to use as a starting point for your own workspace has changed. The **Car Dashboard** sample was replaced by a **Customer Service** sample. The new sample showcases how to use content catalog intents and other newer features to build a bot. It can answer common questions, such as inquiries about store hours and locations, and illustrates how to use a node with slots to schedule in-store appointments.

HTML rendering was added to Try it out
:   The "Try it out" pane now renders HTML formatting that is included in response text. Previously, if you included a hypertext link as an HTML anchor tag in a text response, you would see the HTML source in the "Try it out" pane during testing. It used to look like this:

    `Contact us at <a href="https://www.ibm.com">ibm.com</a>.`

    Now, the hypertext link is rendered as if on a web page. It is displayed like this:

    `Contact us at` [ibm.com](https://www.ibm.com){: external}.

    Remember, you must use the appropriate type of syntax in your responses for the client application to which you will deploy the conversation. Only use HTML syntax if your client application can interpret it properly. Other integration channels might expect other formats.

Deployment changes
:   The **Test in Slack** option was removed.

## 11 May 2018
{: #watson-assistant-may112018}
{: release-note}

Information security
:   The documentation includes some new details about data privacy. Read more in [Information security](/docs/assistant?topic=assistant-information-security){: external}.

## 7 May 2018
{: #watson-assistant-may072018}
{: release-note}

Sydney, Australia data center opens
:   You can now create {{site.data.keyword.conversationshort}} service instances that are hosted in the Sydney, Australia data center. See [IBM Cloud global data centers](https://www.ibm.com/cloud/data-centers/){: external} for more details.

## 4 April 2018
{: #watson-assistant-apr042018}
{: release-note}

Search dialogs
:   You can now [search dialog nodes](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-search){: external} for a given word or phrase.

## 15 March 2018
{: #watson-assistant-mar152018}
{: release-note}

Introducing {{site.data.keyword.conversationfull}}
:   {{site.data.keyword.ibmwatson}} Conversation has been renamed. It is now called {{site.data.keyword.conversationfull}}. The name change reflects the fact that {{site.data.keyword.conversationshort}} is expanding to provide prebuilt content and tools that help you more easily share the virtual assistants you build. Read [this blog post](https://www.ibm.com/blogs/watson/2018/03/the-future-of-watson-conversation-watson-assistant/){: external} for more details.

New REST APIs and SDKs are available for {{site.data.keyword.conversationshort}}
:   The new APIs are functionally identical to the existing Conversation APIs, which continue to be supported. For more information about the {{site.data.keyword.conversationshort}} APIs, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v1){: external}.

Dialog enhancements
:   The following features were added to the dialog tool:

    - Simple variable name and value fields are now available that you can use to add context variables or update context variable values. You do not need to open the JSON editor unless you want to. See [Defining a context variable](/docs/assistant?topic=assistant-dialog-runtime-context#dialog-runtime-context-var-define){: external} for more details.
    - Organize your dialog by using folders to group together related dialog nodes. See [Organizing the dialog with folders](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-folders){: external} for more details.
    - Support was added for customizing how each dialog node participates in user-initiated digressions away from the designated dialog flow. See [Digressions](/docs/assistant?topic=assistant-dialog-runtime#dialog-runtime-digressions){: external} for more details.

Search intents and entities
:   A new search feature has been added that allows you to [search intents](/docs/assistant?topic=assistant-intents#intents-search){: external} for user examples, intent names, or descriptions, or to [search entity](/docs/assistant?topic=assistant-entities#entities-search){: external} values and synonyms.

Content catalogs
:   The new [content catalogs](/docs/assistant?topic=assistant-catalog#catalog-add){: external} contain a single category of prebuilt common intents and entities that you can add to your application. For example, most applications require a general #greeting-type intent that starts a dialog with the user. You can add it from the content catalog rather than building your own.

Enhanced user metrics
:   The Improve component has been enhanced with additional user metrics and logging statistics. For example, the Overview page includes several new, detailed graphs that summarize interactions between users and your application, the amount of traffic for a given time period, and the intents and entities that were recognized most often in user conversations.

## 12 March 2018
{: #watson-assistant-mar122018}
{: release-note}

New date and time methods
:   Methods were added that make it easier to perform date calculations from the dialog. See [Date and time calculations](/docs/assistant?topic=assistant-dialog-methods#dialog-methods-date-time-calculations){: external} for more details.

## 16 February 2018
{: #watson-assistant-feb162018}
{: release-note}

Dialog node tracing
:   When you use the "Try it out" pane to test a dialog, a location icon is displayed next to each response. You can click the icon to highlight the path that your assistant traversed through the dialog tree to arrive at the response. See [Building a dialog](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-test){: external} for details.

New API version
:   The current API version is now `2018-02-16`. This version introduces the following changes:

    - A new `include_audit` parameter is now supported on most GET requests. This is an optional boolean parameter that specifies whether the response should include the audit properties (`created` and `updated` timestamps). The default value is `false`. (If you are using an API version earlier than `2018-02-16`, the default value is `true`.) For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v1){: external}.

    - Responses from API calls using the new version include only properties with non-`null` values.

    - The `output.nodes_visited` and `output.nodes_visited_details` properties of message responses now include nodes with the following types, which were previously omitted:

    - Nodes with `type`=`response_condition`
    - Nodes with `type`=`event_handler` and `event_name`=`input`

## 9 February 2018
{: #watson-assistant-feb092018}
{: release-note}

Dutch system entities (Beta)
:   Dutch language support has been enhanced to include the availability of [System entities](/docs/assistant?topic=assistant-system-entities){: external} in beta release. See [Supported languages](/docs/assistant?topic=assistant-language-support){: external} for details.

## 29 January 2018
{: #watson-assistant-jan292018}
{: release-note}

- The {{site.data.keyword.conversationshort}} REST API now supports new request parameters:
    - Use the `append` parameter when updating a workspace to indicate whether the new workspace data should be added to the existing data, rather than replacing it. For more information, see [Update workspace](https://cloud.ibm.com/apidocs/assistant/assistant-v1?curl=#update-workspace){: external}.
    - Use the `nodes_visited_details` parameter when sending a message to indicate whether the response should include additional diagnostic information about the nodes that were visited during processing of the message. For more information, see [Send message](https://cloud.ibm.com/apidocs/assistant/assistant-v1?curl=#message){: external}.

## 23 January 2018
{: #watson-assistant-jan232018}
{: release-note}

Unable to retrieve list of workspaces
:   If you see this or similar error messages when working in the tooling, it might mean that your session has expired. Log out by choosing **Log out** from the **User information** icon, and then log back in.

## 8 December 2017
{: #watson-assistant-dec082017}
{: release-note}

Log data access across instances (Premium users only)
:   If you are a {{site.data.keyword.conversationshort}} Premium user, your premium instances can optionally be configured to allow access to log data from workspaces across your different premium instances.

Copy nodes
:   You can now duplicate a node to make a copy of it and its children. This feature is helpful if you build a node with useful logic that you want to reuse elsewhere in your dialog. See [Copying a dialog node](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-copy-node){: external} for more information.

Capture groups in pattern entities
:   You can identify groups in the regular expression pattern that you define for an entity. Identifying groups is useful if you want to be able to refer to a subsection of the pattern later. For example, your entity might have a regex pattern that captures US phone numbers. If you identify the area code segment of the number pattern as a group, then you can subsequently refer to that group to access just the area code segment of a phone number. See [Defining entities](/docs/assistant?topic=assistant-entities#entities-creating-task){: external} for more information.

## 6 December 2017
{: #watson-assistant-dec062017}
{: release-note}

{{site.data.keyword.openwhisk}} integration (Beta)
:   Call {{site.data.keyword.openwhisk}} (formerly IBM OpenWhisk) actions directly from a dialog node. This feature enables you to, for example, call an action to retrieve weather information from within a dialog node, and then condition on the returned information in the dialog response. Currently, you can call an action from a {{site.data.keyword.openwhisk_short}} instance that is hosted in the US South region from {{site.data.keyword.conversationshort}} instances that are hosted in the US South region. See [Making programmatic calls from a dialog node](/docs/assistant?topic=assistant-dialog-actions-client){: external} for more details.

## 5 December 2017
{: #watson-assistant-dec052017}
{: release-note}

Redesigned UI for Intents and Entities
:   The `Intents` and `Entities` tabs have been redesigned to provide an easier, more efficient workflow when creating and editing entities and intents. See [Defining intents](/docs/assistant?topic=assistant-intents-create-task){: external} and [Defining entities](/docs/assistant?topic=assistant-entities#entities-creating-task){: external} for information about working with these tabs.

## 30 November 2017
{: #watson-assistant-nov302017}
{: release-note}

Eastern Arabic numeral support
:   Eastern Arabic numerals are now supported in Arabic system entities.

## 29 November 2017
{: #watson-assistant-nov292017}
{: release-note}

Improving understanding of user input across workspaces
:   You can now improve a workspace with utterances that were sent to other workspaces within your instance. For example, you might have multiple versions of production workspaces and development workspaces; you can use the same utterance data to improve any of these workspaces. See [Improving across workspaces](/docs/assistant?topic=assistant-logs#logs-deploy-id){: external}.

## 20 November 2017
{: #watson-assistant-nov202017}
{: release-note}

GB18030 compliance
:   GB18030 is a Chinese standard that specifies an extended code page for use in the Chinese market. This code page standard is important for the software industry because the China National Information Technology Standardization Technical Committee has mandated that any software application that is released for the Chinese market after September 1, 2001, be enabled for GB18030. The {{site.data.keyword.conversationshort}} service supports this encoding, and is certified GB18030-compliant.

## 9 November 2017
{: #watson-assistant-nov092017}
{: release-note}

Intent examples can directly reference entities
:   You can now specify an entity reference directly in an intent example. That entity reference, along with all its values or synonyms, is used by the {{site.data.keyword.conversationshort}} service classifier for training the intent. For more information, see [*Entity as example*](/docs/assistant?topic=assistant-intents#intents-entity-as-example){: external} in the [Intents](/docs/assistant?topic=assistant-intents){: external} topic.

    Currently, you can only directly reference closed entities that you define. You cannot directly reference [pattern entities](/docs/assistant?topic=assistant-entities#entities-patterns) or [system entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 8 November 2017
{: #watson-assistant-nov082017}
{: release-note}

{{site.data.keyword.conversationshort}} connector
:   You can use the new {{site.data.keyword.conversationshort}} connector tool to connect your workspace to a Slack or Facebook Messenger app that you own, making it available as a chatbot that Slack or Facebook Messenger users can interact with. This tool is available only for the {{site.data.keyword.Bluemix_notm}} US South region.

## 3 November 2017
{: #watson-assistant-nov032017}
{: release-note}

Dialog updates
:   The following updates make is easier for you to build a dialog. (See [Building a dialog](/docs/assistant?topic=assistant-dialog-build){: external} for details.)

    - You can add a condition to a slot to make it required only if certain conditions are met. For example, you can make a slot that asks for the name of a spouse required only if a previous (required) slot that asks for marital status indicates that the user is married.

    - You can now choose **Skip user input** as the next step for a node. When you choose this option, after processing the current node, your assistant jumps directly to the first child node of the current node. This option is similar to the existing *Jump to* next step option, except that it allows for more flexibility. You do not need to specify the exact node to jump to. At run time, your assistant always jumps to whichever node is the first child node, even if the child nodes are reordered or new nodes are added after the next step behavior is defined.

    - You can add conditional responses for slots. For both Found and Not found responses, you can customize how your assistant responds based on whether certain conditions are met. This feature enables you to check for possible misinterpretations and correct them before saving the value provided by the user in the slot's context variable. For example, if the slot saves the user's age, and uses `@sys-number` in the *Check for* field to capture it, you can add a condition that checks for numbers over 100, and responds with something like, *Please provide a valid age in years.* See [Adding conditions to Found and Not found responses](/docs/assistant?topic=assistant-dialog-slots#dialog-slots-handler-next-steps){: external} for more details.

    - The interface you use to add conditional responses to a node has been redesigned to make it easier to list each condition and its response. To add node-level conditional responses, click **Customize**, and then enable the **Multiple responses** option.

     The **Multiple responses** toggle sets the feature on or off for the node-level response only. It does not control the ability to define conditional responses for a slot. The slot multiple response setting is controlled separately.

    - To keep the page where you edit a slot simple, you now select menu options to a.) add a condition that must be met for the slot to be processed, and b.) add conditional responses for the Found and Not found conditions for a slot. Unless you choose to add this extra functionality, the slot condition and multiple responses fields are not displayed, which declutters the page and makes it easier to use.

## 25 October 2017
{: #watson-assistant-oct252017}
{: release-note}

Updates to Simplified Chinese
:   Language support has been enhanced for Simplified Chinese. This includes intent classification improvements using character-level word embeddings, and the availability of system entities. Note that the {{site.data.keyword.conversationshort}} service learning models may have been updated as part of this enhancement, and when you retrain your model any changes will be applied.

Updates to Spanish
:   Improvements have been made to Spanish intent classification, for very large datasets.

## 11 October 2017
{: #watson-assistant-oct112017}
{: release-note}

Updates to Korean
:   Language support has been enhanced for Korean. Note that the {{site.data.keyword.conversationshort}} service learning models may have been updated as part of this enhancement, and when you retrain your model any changes will be applied.

## 3 October 2017
{: #watson-assistant-oct032017}
{: release-note}

Pattern-defined entities (Beta)
:   You can now define specific patterns for an entity, using regular expressions. This can help you identify entities that follow a defined pattern, for example SKU or part numbers, phone numbers, or email addresses. See [Pattern-defined entities](/docs/assistant?topic=assistant-entities#entities-patterns){: external} for additional details.

    - You can add either synonyms or patterns for a single entity value; you cannot add both.
    - For each entity value, there can be a maximum of up to 5 patterns.
    - Each pattern (regular expression) is limited to 128 characters.
    - Importing or exporting via a CSV file does not currently support patterns.
    - The REST API does not support direct access to patterns, but you can retrieve or modify patterns using the `/values` endpoint.

Fuzzy matching filtered by dictionary (English only)
:   An improved version of fuzzy matching for entities is now available, for English. This improvement prevents the capturing of some common, valid English words as fuzzy matches for a given entity. For example, fuzzy matching will not match the entity value `like` to `hike` or `bike`, which are valid English words, but will continue to match examples such as `lkie` or `oike`.

## 27 September 2017
{: #watson-assistant-sep272017}
{: release-note}

Condition builder updates
:   The control that is displayed to help you define a condition in a dialog node has been updated. Enhancements include support for listing available context variable names after you enter the $ to begin adding a context variable.

## 31 August 2017
{: #watson-assistant-aug312017}
{: release-note}

Improve section rollback
:   The median conversation time metric, and corresponding filters, are being temporarily removed from the Overview page of the Improve section. This removal will prevent the calculation of certain metrics from causing the median conversation time metric, and the conversations over time graph, to display inaccurate information. IBM regrets removing functionality from the tool, but is committed to ensuring that we are communicating accurate information to users.

Dialog node names
:   You can now assign any name to a dialog node; it does not need to be unique. And you can subsequently change the node name without impacting how the node is referenced internally. The name you specify is saved as a title attribute of the node in the workspace JSON file and the system uses a unique ID that is stored in the name attribute to reference the node.

## 23 August 2017
{: #watson-assistant-aug232017}
{: release-note}

Updates to Korean, Japanese, and Italian
:   Language support has been enhanced for Korean, Japanese, and Italian. Note that the {{site.data.keyword.conversationshort}} service learning models may have been updated as part of this enhancement, and when you retrain your model any changes will be applied.

## 10 August 2017
{: #watson-assistant-aug102017}
{: release-note}

Accent normalization
:   In a conversational setting, users may or may not use accents while interacting with the {{site.data.keyword.conversationshort}} service. As such, an update has been made to the algorithm so that accented and non-accented versions of words are treated the same for intent detection and entity recognition.

    However, for some languages like Spanish, some accents can alter the meaning of the entity. Thus, for entity detection, although the original entity may implicitly have an accent, your assistant can also match the non-accented version of the same entity, but with a slightly lower confidence score.

    For example, for the word `barrió`, which has an accent and corresponds to the past tense of the verb `barrer` (to sweep), your assistant can also match the word `barrio` (neighborhood), but with a slightly lower confidence.

    The system will provide the highest confidence scores in entities with exact matches. For example, `barrio` will not be detected if `barrió` is in the training set; and `barrió` will not be detected if `barrio` is in the training set.

    You are expected to train the system with the proper characters and accents. For example, if you are expecting `barrió` as a response, then you should put `barrió` into the training set.

    Although not an accent mark, the same applies to words using, for example, the Spanish letter `ñ` vs. the letter `n`, such as `uña` vs. `una`. In this case the letter `ñ` is not simply an `n` with an accent; it is a unique, Spanish-specific letter.

    You can enable fuzzy matching if you think your customers will not use the appropriate accents, or misspell words (including, for example, putting a `n` instead of a `ñ`), or you can explicitly include them in the training examples.

    **Note:** Accent normalization is enabled for Portuguese, Spanish, French, and Czech.

Workspace opt-out flag
:   The {{site.data.keyword.conversationshort}} REST API now supports an opt-out flag for workspaces. This flag indicates that workspace training data such as intents and entities are not to be used by IBM for general service improvements. For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v1?curl=#data-collection){: external}

## 7 August 2017
{: #watson-assistant-aug072017}
{: release-note}

`Next` and `last` date interpretation
:   The {{site.data.keyword.conversationshort}} service treats `last` and `next` dates as referring to the most immediate last or next day referenced, which may be in either the same or a previous week. See the [system entities](/docs/assistant?topic=assistant-system-entities#system-entities-sys-date-time){: external} topic for additional information.

## 3 August 2017
{: #watson-assistant-aug032017}
{: release-note}

Fuzzy matching for additional languages (Beta)
:   Fuzzy matching for entities is now available for additional languages, as noted in the [Supported languages](/docs/assistant?topic=assistant-language-support){: external} topic.

Partial match (Beta - English only)
:   Fuzzy matching will now automatically suggest substring-based synonyms present in user-defined entities, and assign a lower confidence score as compared to the exact entity match. See [Fuzzy matching](/docs/assistant?topic=assistant-entities#entities-fuzzy-matching){: external} for details.

## 28 July 2017
{: #watson-assistant-jul282017}
{: release-note}

Updates
:   This release includes the following updates:

    - When you set bidirectional preferences for the tooling, you can now specify the graphical user interface direction.
    - The color scheme of the tooling was updated to be consistent with other Watson services and products.

## 19 July 2017
{: #watson-assistant-jul192017}
{: release-note}

REST API now supports access to dialog nodes
:   The {{site.data.keyword.conversationshort}} REST API now supports access to dialog nodes. For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v1?curl=#listdialognodes){: external}.

## 14 July 2017
{: #watson-assistant-jul142017}
{: release-note}

Slots enhancement
:   The slots functionality of dialogs was enhanced. For example, a *slot_in_focus* property was added that you can use to define a condition that applies to a single slot only. See [Gathering information with slots](/docs/assistant?topic=assistant-dialog-slots){: external} for details.

## 12 July 2017
{: #watson-assistant-jul122017}
{: release-note}

Support for Czech
:   Czech language support has been introduced; please see the [Supported languages](/docs/assistant?topic=assistant-language-support){: external} topic for additional details.

## 11 July 2017
{: #watson-assistant-jul112017}
{: release-note}

Test in Slack
:   You can use the new **Test in Slack** tool to quickly deploy your workspace as a Slack bot user for testing purposes. This tool is available only for the {{site.data.keyword.Bluemix_notm}} US South region.

Updates to Arabic
:   Arabic language support has been enhanced to include absolute scoring per intent, and the ability to mark intents as irrelevant; please see the [Supported languages](/docs/assistant?topic=assistant-language-support){: external} topic for additional details. Note that the {{site.data.keyword.conversationshort}} service learning models may have been updated as part of this enhancement, and when you retrain your model any changes will be applied.

## 23 June 2017
{: #watson-assistant-jun232017}
{: release-note}

Updates to Korean
:   Korean language support has been enhanced; please see the [Supported languages](/docs/assistant?topic=assistant-language-support){: external} topic for additional details. Note that the {{site.data.keyword.conversationshort}} service learning models may have been updated as part of this enhancement, and when you retrain your model any changes will be applied.

## 22 June 2017
{: #watson-assistant-jun222017}
{: release-note}

Introducing slots
:   It is now easier to collect multiple pieces of information from a user in a single node by adding slots. Previously, you had to create several dialog nodes to cover all the possible combinations of ways that users might provide the information. With slots, you can configure a single node that saves any information that the user provides, and prompts for any required details that the user does not. See [Gathering information with slots](/docs/assistant?topic=assistant-dialog-slots){: external} for more details.

Simplified dialog tree
:   The dialog tree has been redesigned to improve its usability. The tree view is more compact so it is easier to see where you are within it. And the links between nodes are represented in a way that makes it easier to understand the relationships between the nodes.

## 21 June 2017
{: #watson-assistant-jun212017}
{: release-note}

Arabic support
:   Language support for Arabic is now generally available. For details, see [Configuring bidirectional languages](/docs/assistant?topic=assistant-language-support#language-support-configure-bidirectional){: external}.

Language updates
:   The {{site.data.keyword.conversationshort}} service algorithms have been updated to improve overall language support. See the [Supported languages](/docs/assistant?topic=assistant-language-support){: external} topic for details.

## 16 June 2017
{: #watson-assistant-jun162017}
{: release-note}

Recommendations (Beta - Premium users only)
:   The Improve panel also includes a **Recommendations** page that recommends ways to improve your system by analyzing the conversations that users have with your chatbot, and taking into account your system's current training data and response certainty.

## 14 June 2017
{: #watson-assistant-jun142017}
{: release-note}

Fuzzy matching for additional languages (Beta)
:   Fuzzy matching for entities is now available for additional languages, as noted in the [Supported languages](/docs/assistant?topic=assistant-language-support){: external} topic. You can turn on fuzzy matching per entity to improve the ability of your assistant to recognize terms in user input with syntax that is similar to the entity, without requiring an exact match. The feature is able to map user input to the appropriate corresponding entity despite the presence of misspellings or slight syntactical differences. For example, if you define giraffe as a synonym for an animal entity, and the user input contains the terms giraffes or girafe, the fuzzy match is able to map the term to the animal entity correctly. See [Fuzzy matching](/docs/assistant?topic=assistant-entities#entities-fuzzy-matching){: external} for details.

## 13 June 2017
{: #watson-assistant-jun132017}
{: release-note}

User conversations
:   The Improve panel now includes a **User conversations** page, which provides a list of user interactions with your chatbot that can be filtered by keyword, intent, entity, or number of days. You can open individual conversations to correct intents, or to add entity values or synonyms.

Regex change
:   The regular expressions that are supported by SpEL functions like find, matches, extract, replaceFirst, replaceAll and split have changed. A group of regular expression constructs are no longer allowed, including look-ahead, look-behind, possessive repetition and backreference constructs. This change was necessary to avoid a security exposure in the original regular expression library.

## 12 June 2017
{: #watson-assistant-jun122017}
{: release-note}

Updates
:   This release includes the following updates:
    - The maximum number of workspaces that you can create with the **Lite** plan (formerly named the Free plan) changed from 3 to 5.
    - You can now assign any name to a dialog node; it does not need to be unique. And you can subsequently change the node name without impacting how the node is referenced internally. The name you specify is treated as an alias and the system uses its own internal identifier to reference the node.
    - You can no longer change the language of a workspace after you create it by editing the workspace details. If you need to change the language, you can export the workspace as a JSON file, update the language property, and then import the JSON file as a new workspace.

## 6 June 2017
{: #watson-assistant-jun062017}
{: release-note}

Learn
:   A new *Learn about {{site.data.keyword.conversationfull}}* page is available that provides getting started information and links to service documentation and other useful resources. To open the page, click the icon in the page header.

Bulk export and delete
:   You can now simultaneously export a number of intents or entities to a CSV file, so you can then import and reuse them for another {{site.data.keyword.conversationshort}} application. You can also simultaneously select a number of entities or intents for deletion in bulk.

Updates to Korean
:   Korean tokenizers have been updated to address informal language support. IBM continues to work on improvements to entity recognition and classification.

Emoji support
:   Emojis added to intent examples, or as entity values, will now be correctly classified/extracted.

    Only emojis that are included in your training data will be correctly and consistently identified; emoji support may not correctly classify similar emojis with different color tones or other variations.

Entity stemming (Beta - English only)
:   The fuzzy matching beta feature recognizes entities and matches them based on the stem form of the entity value. For example, this feature correctly recognizes `bananas` as being similar to `banana`, and `run` being similar to `running` as they share a common stem form. For more information, see [Fuzzy matching](/docs/assistant?topic=assistant-entities#entities-fuzzy-matching){: external}.

Workspace import progress
:   When you import a workspace from a JSON file, a tile for the workspace is displayed immediately, in which information about the progress of the import is displayed.

Reduced training time
:   Multiple models are now trained in parallel, which noticeably reduces the training time for large workspaces.

## 26 May 2017
{: #watson-assistant-may262017}
{: release-note}

New API version
:   The current API version is now `2017-05-26`. This version introduces the following changes:

    - The schema of ErrorResponse objects has changed. This change affects all endpoints and methods. For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant){: external}.
    - The internal schema used to represent dialog nodes in exported workspace JSON has changed. If you use the `2017-05-26` API to import a workspace that was exported using an earlier version, some dialog nodes might not import correctly. For best results, always import a workspace using the same version that was used to export it.

## 25 May 2017
{: #watson-assistant-may252017}
{: release-note}

Manage context variables
:   You can now manage context variables in the "Try it out" pane. Click the **Manage context** link to open a new pane where you can set and check the values of context variables as you test the dialog. See [Testing your dialog](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-test){: external} for more information.

## 16 May 2017
{: #watson-assistant-may162017}
{: release-note}

Updates
:   This release includes the following updates:

    - A **Car Dashboard** sample workspace is now available when you open the tool. To use the sample as a starting point for your own workspace, edit the workspace. If you want to use it for multiple workspaces, then duplicate it instead. The sample workspace does not count toward your subscription workspace total unless you use it.
    - It is now easier to navigate the tool. The navigation menu options are available from the side of the main page instead of the top. In the page header, breadcrumb links display that show you where you are. You can now switch between service instances from the Workspaces page. To get there quickly, click **Back to workspaces** from the navigation menu. If you have multiple service instances, the name of the current instance is displayed. You can click the **Change** link beside it to choose another instance.
    - When you create a dialog, two nodes are now added to it for you: 1) a **Welcome** node at the start the dialog tree that contains the greeting to display to the user and 2) an **Anything else** node at the end of the tree that catches any user inquiries that are not recognized by other nodes in the dialog and responds to them. See [Creating a dialog](/docs/assistant?topic=assistant-dialog-build){: external} for more details.
    - When you are testing a dialog in the "Try it out" pane, you can now find and resubmit a recent test utterance by pressing the Up key to cycle through your previous inputs.
    - Experimental Korean language support for 5 system entities (`@sys-date`, `@sys-time`, `@sys-currency`, `@sys-number`, `@sys-percentage`) is now available. There are known issues for some of the numeric entities, and limited support for informal language input.
    - An Overview page is available from the Improve tab. The page provides a summary of interactions with your bot. You can view the amount of traffic for a given time period, as well as the intents and entities that were recognized most often in user conversations. For additional information, see [Using the Overview page](/docs/assistant?topic=assistant-logs-overview){: external}.

## 27 April 2017
{: #watson-assistant-apr272017}
{: release-note}

System entities
:   The following system entities are now available as beta features in English only:

    - sys-location: Recognizes references to locations, such as towns, cities, and countries, in user utterances.
    - sys-person: Recognizes references to people's names, first and last, in user utterances.

    For more information, see the [System entities reference](/docs/assistant?topic=assistant-system-entities){: external}.

Fuzzy matching for entities
:   Fuzzy matching for entities is a beta feature that is now available in English. You can turn on fuzzy matching per entity to improve the ability of your assistant to recognize terms in user input with syntax that is similar to the entity, without requiring an exact match. The feature is able to map user input to the appropriate corresponding entity despite the presence of misspellings or slight syntactical differences. For examples, if you define **giraffe** as a synonym for an animal entity, and the user input contains the terms *giraffes* or *girafe*, the fuzzy match is able to map the term to the animal entity correctly. See [Defining entities](/docs/assistant?topic=assistant-entities#entities-fuzzy-matching){: external} and search for `Fuzzy Matching` for details.

## 18 April 2017
{: #watson-assistant-apr182017}
{: release-note}

Updates
:   This release includes the following updates:

    - The {{site.data.keyword.conversationshort}} REST API now supports access to the following resources:
        - entities
        - entity values
        - entity value synonyms
        - logs

        For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v1){: external}.

    - The behavior of the /messages `POST` method has changed the handling of entities and intents specified as part of the message input:
        - If you specify intents on input, your assistant uses the intents you specify, but uses natural language processing to detect entities in the user input.
        - If you specify entities on input, your assistant uses the entities you specify, but uses natural language processing to detect intents in the user input.

        The behavior has not changed for messages that specify both intents and entities, or for messages that specify neither.

    - The option to mark user input as irrelevant is now available for all supported languages. This is a beta feature.

    - A new Credentials tab provides a single place where you can find all of the information you need for connecting your application to a workspace (such as the {{site.data.keyword.conversationshort}} credentials and workspace ID), as well as other deployment options. To access the Credentials tab for your workspace, click the icon and select **Credentials**.

## 9 March 2017
{: #watson-assistant-mar092017}
{: release-note}

REST API updates
:   The {{site.data.keyword.conversationshort}} REST API now supports access to the following resources:

    - workspaces
    - intents
    - examples
    - counterexamples

    For more information, see the [API Reference](https://cloud.ibm.com/apidocs/assistant/assistant-v1){: external}.

## 7 March 2017
{: #watson-assistant-mar072017}
{: release-note}

Intent name restrictions
:   The use of `.` or `..` as an intent name causes problems and is no longer supported. You cannot rename or delete an intent with this name; to change the name, export your intents to a file, rename the intent in the file, and import the updated file into your workspace. Paying customers can contact support for a database change.

## 1 March 2017
{: #watson-assistant-mar012017}
{: release-note}

System entities are now enabled in German
:   System entities are now enabled in German.

## 22 February 2017
{: #watson-assistant-feb222017}
{: release-note}

Messages are now limited to 2,048 characters
: Messages are now limited to 2,048 characters.

## 3 February 2017
{: #watson-assistant-feb032017}
{: release-note}

Updates
:   This release includes the following updates:

    - We changed how intents are scored and added the ability to mark input as irrelevant to your application. For details, see [Defining intents](/docs/assistant?topic=assistant-intents){: external} and search for `Mark as irrelevant`.

    - This release introduced a major change to the workspace. To benefit from the changes, you must manually upgrade your workspace.

    - The processing of **Jump to** actions changed to prevent loops that can occur under certain conditions. Previously, if you jumped to the condition of a node and neither that node nor any of its peer nodes had a condition that was evaluated as true, the system would jump to the root-level node and look for a node whose condition matched the input. In some situations this processing created a loop, which prevented the dialog from progressing.

     Under the new process, if neither the target node nor its peers is evaluated as true, the dialog turn is ended. To reimplement the old model, add a final peer node with a condition of `true`. In the response, use a **Jump to** action that targets the condition of the first node at the root level of your dialog tree.

## 11 January 2017
{: #watson-assistant-jan112017}
{: release-note}

Customize node titles
:   In this release, you can customize node titles in dialog.

## 22 December 2016
{: #watson-assistant-dec222016}
{: release-note}

Node title section
:   In this release, dialog nodes display a new section for `node title`. The ability to customize the `node title` is not available. When collapsed, the `node title` displays the `node condition` of the dialog node. If there is not a `node condition`, "Untitled Node" is displayed as the title.

## 19 December 2016
{: #watson-assistant-dec192016}
{: release-note}

Dialog editor UI changes
:   Several changes make the dialog editor easier and more intuitive to use:

    - A larger editing view makes it easier to view all the details of a node as you work on it.
    - A node can contain multiple responses, each triggered by a separate condition. For more information see [Multiple responses](/docs/assistant?topic=assistant-dialog-overview#dialog-overview-responses){: external}.

## 5 December 2016
{: #watson-assistant-dec052016}
{: release-note}

Updates
:   This release includes the following updates:

    - New languages are supported, all in Experimental mode: German, Traditional Chinese, Simplified Chinese, and Dutch.
    - Two new system entities are available: @sys-date and @sys-time. For details, see [System entities](/docs/assistant?topic=assistant-system-entities){: external}.

## 21 October 2016
{: #watson-assistant-oct212016}
{: release-note}

Updates
:   This release includes the following updates:

    - The {{site.data.keyword.conversationshort}} service now provides system entities, which are common entities that can be used across any use case. For details, see [Defining entities](/docs/assistant?topic=assistant-entities){: external} and search for `Enabling system entities`.
    - You can now view a history of conversations with users on the Improve page. You can use this to understand your bot's behavior. For details, see [Improving your skill](/docs/assistant?topic=assistant-logs){: external}.
    - You can now import entities from a comma-separated value (CSV) file, which helps with when you have a large number of entities. For details, see [Defining entities](/docs/assistant?topic=assistant-entities){: external} and search for `Importing entities`.

## 20 September 2016
{: #watson-assistant-sep202016}
{: release-note}

New version 2016-09-20

:   To take advantage of the changes in a new version, change the value of the `version` parameter to the new date. If you're not ready to update to this version, don't change your version date.

    - version **2016-09-20**: `dialog_stack` changed from an array of strings to an array of JSON objects.

## 29 August 2016
{: #watson-assistant-aug292016}
{: release-note}

Updates
:   This release includes the following updates:

    - You can move dialog nodes from one branch to another, as siblings or peers. For details, see [Moving a dialog node](/docs/assistant?topic=assistant-dialog-tasks#dialog-tasks-move-node){: external}.
    - You can expand the JSON editor window.
    - You can view chat logs of your bot's conversations to help you understand it's behavior. You can filter by intents, entities, date, and time. For details, see [Improving your skill](/docs/assistant?topic=assistant-logs){: external}.

## 11 July 2016
{: #watson-assistant-jul212016}
{: release-note}

General Availability
:    This General Availability release enables you to work with entities and dialogs to create a fully functioning bot.

## 18 May 2016
{: #watson-assistant-may182016}
{: release-note}

Experimental release
:   This Experimental release of the {{site.data.keyword.conversationshort}} introduces the user interface and enables you to work with workspaces, intents, and examples.
