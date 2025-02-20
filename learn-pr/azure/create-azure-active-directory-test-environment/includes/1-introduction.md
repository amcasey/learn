<!-- 1. Topic sentence(s) --------------------------------------------------------------------------------

    Goal: familiarize the learner with the area covered in this module

    Heading: none

    Example: "Azure Logic Apps let you automate your business processes and run them in the cloud."

    Recommended: visual like an image, table, list, etc. that supports the topic sentence(s)

    [Introduction unit guidance](https://review.docs.microsoft.com/learn-docs/docs/id-guidance-introductions?branch=main#rule-use-the-standard-module-introduction-format)
-->
A Microsoft Entra tenant includes the tenant's users, groups, and apps and is used to perform identity and access management functions for tenant resources.  You can create different tenants and resources to represent different application environments, such as production and test.

<!--TODO: add a visual element -->

<!-- 2. Scenario -----------------------------------------------------------------------------------------

    Goal: describe the real-world scenario this module will use to illustrate the concepts

    Heading: "## Example scenario"

    Example: "Suppose you work at an athletic shoe company on the marketing team. You're launching a new basketball shoe created by a celebrity athlete. Previous launches resulted in a social media frenzy as people shared stories and photos of themselves wearing their new shoes. The marketing team wants to monitor hundreds of social media sites, blogs, and websites to determine consumer reaction. There will be more data than you can process manually. You would like a cloud-hosted system that automates monitoring, text analytics, database storage, and email notifications."

    Recommended: an image that visualizes the scenario, use the image markdown extension (https://review.docs.microsoft.com/help/contribute/markdown-reference?branch=main#images)

    Optional: a "scenario video" that visualizes the scenario

    [Scenario guidance](https://review.docs.microsoft.com/learn-docs/docs/id-guidance-scenarios)
    [Scenario video guidance](TBD)
 -->
## Example scenario

Suppose you work on a development team that creates internal apps for a retail company. Your team recently released a sales team dashboard for sales managers to manage their direct reports and help them meet their targets. You now need a Microsoft Entra test environment for a CI/CD pipeline that automates the deployment of the web app, the configuration of Azure App Service authentication, and the execution of integration tests as a user.

In this module, your team will set up a Microsoft Entra test environment to help move your web app through the development, test, and production lifecycle.  You'll need a Microsoft Entra tenant, which contains app registrations to represent your application and test clients, test users, and optionally policies to protect resources.

:::image type="content" source="../media/pipeline.png" alt-text="Diagram showing the components of a CI/CD pipeline.":::

<!-- 3. Prose table-of-contents --------------------------------------------------------------------------

    Goal: List the activities the learner will do in this content. This differs from the title and the learning objectives. The title and the learning objectives are "outcome focused"; that is, they describe the skills the learner will acquire as a result of consuming this content. By contrast, here you should be specific about what the learning will **do** in order to acquire those skills. The format can be either prose or bulleted-list; however, a list will yield better results when transformed into other output types such as PowerPoint.

    Heading: "## What will we be doing?"

    Example: "Here, you'll create a business workflow using Azure Logic Apps to automate the processing of tweets:
                * **Launch**: when a new tweet is available
                * **Process**: determine if the sentiment of the tweet is positive or negative
                * **Route**: branch based on the sentiment score"

 -->
## What will we be doing?

In this module, you will:

- Decide whether to use a production Microsoft Entra tenant or a separate tenant for your test environment
- Set up a dedicated test tenant in Microsoft Entra ID
- Create a test user in the test tenant
- Create an app registration to use as a test client for your web app
- Add policies to the test tenant

<!-- 4. Terminal learning objective ----------------------------------------------------------------------

    Goal: This is a restatement of the module title into a complete sentence. You have more room here to convey the main goal than in a space-limited title. Make it outcome-focused so it describes the main skill the learner will acquire as a result of this training. In other words, it should answer the question: "what is the key thing the learner will be able to do as a result of consuming this training?"

    Heading: "## What is the main goal?"

    Example: "By the end of this session, you'll be able to create workflows which route and process data using Azure Logic Apps and its built-in connectors."

 -->
## What is the main goal?

By the end of this session, you'll be able to set up a test environment in Microsoft Entra ID for testing applications.

<!-- Do **not** include any other content like learning objectives, prerequisites, unit summary, "next unit" lead-in, or references. -->
