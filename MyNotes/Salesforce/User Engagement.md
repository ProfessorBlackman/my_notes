## User Engagement
| **Scenario**                   | **Description**                                                                                                       | **Examples**                                                                                              |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Onboarding                     | Show users where to begin and what’s new or changed. Get them to the “aha moment” quickly.                            | - First time in trial or new feature area <br>- Setting up a new feature<br>- First time in a new release |
| Feature discovery and adoption | Help beginners become experts. Help experienced users learn new things. Raise awareness of new features and releases. | - New feature enabled<br>- Encourage best practices                                                       |
| Troubleshooting help           | Provide just-in-time prompts that help users learn by doing. Offer reliable resources and access to support.          | - User is off course  <br>- User has a question                                                           |
| Deeper learning                | Give users the skills and information they need to get as much value as possible out of your product or application.  | User wants a deeper understanding of a new feature                                                        |

### Components and Patterns
| **Component**    | **Description**                                                                                                                                                      | **Programmatic or Declarative?** |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| Welcome Mat      | Provide getting started resources the first time that users log in to Lightning Experience.                                                                          | Programmatic                     |
| Guidance Center  | The Trailhead icon in the header opens a menu of contextual help topics, Trailhead modules, and more items selected by Salesforce or added by your company.          | Declarative                      |
| Prompts          | Use a floating, targeted, or docked prompt to let users know about new features, news, important announcements, or helpful guidance for the page they're working on. | Declarative                      |
| Popovers         | Use a feature popover to point to a lower-level component on the page to provide tips and best practices.                                                            | Programmatic                     |
| Empty State      | Replace a blank section with instructions on next steps.                                                                                                             | Programmatic                     |
| Field-level Help | Detail the purpose and function of a standard or custom field.                                                                                                       | Declarative                      |
| Setup Assistant  | Centralized list of tasks designed to help users onboard organizations, clouds, or features.                                                                         | Programmatic                     |
| Walkthrough      | Hands-on interactive tour, guiding users through a series of onboarding steps.                                                                                       | Declarative                      |


**Which components are best suited for each scenario:**

| **Component**    | **Onboarding** | **Adoption and Discovery** | **Troubleshooting** | **Deeper Learning** |
| :--------------- | -------------- | -------------------------- | ------------------- | ------------------- |
| Welcome mat      | :luc_check:    |                            |                     | :luc_check:         |
| Guidance Center  | :luc_check:    |                            | :luc_check:         | :luc_check:         |
| Prompts          | :luc_check:    | :luc_check:                | :luc_check:         | :luc_check:         |
| Popovers         | :luc_check:    | :luc_check:                | :luc_check:         | :luc_check:         |
| Empty State      |                | :luc_check:                | :luc_check:         | :luc_check:         |
| Field-level Help |                | :luc_check:                | :luc_check:         |                     |
| Walkthrough      | :luc_check:    | :luc_check:                |                     | :luc_check:         |

### Push Method vs Pull Method
Use the push method when users may not notice or seek out help, but would benefit from assistance. Present content to the user even though they don’t seek it out. For example, show a welcome mat (1) upon first login or display a prompt when a user lands on the Account homepage. Prompts, popovers, and walkthroughs are examples of the push method.

Use the pull method when the user is motivated to seek help. This is where the Guidance Center shines because it’s always available to open and help users when they need it. Another common example is the infobubble (2), which opens a tooltip when you hover over an icon.
![[Pasted image 20240516102034.png]]
### Even More User Engagement Options

There are some additional features, options, and components that you might not even have considered as user engagement.

- Utility Bar Notes—Give your users quick access to common productivity tools in a fixed footer. Utilities open in docked panels.  
    
- Rich Text Component—Add text and simple HTML markup to your Lightning pages.  
    
- Guidance for Success on Path—At each step on the path, help users succeed with step-specific guidance, such as tips, links, and information about company policies.  
    
- Custom Notification from a Flow—Send customized notifications when important events occur. For example, alert an account owner when a new support case is logged.  
    
- Einstein Analytics In-Dashboard Videos—Drive adoption and engagement with educational videos. Provide customized instruction that helps users get the most out of each dashboard and its charts.

### Resources
- [_Lightning Design System: User Engagement Overview_](https://www.lightningdesignsystem.com/guidelines/user-engagement/overview/)  
- [_Salesforce Help: Custom Help Content_](https://help.salesforce.com/articleView?id=customhelp_about.htm&language=en_US&_ga=2.168661153.1872851458.1702926453-1215546439.1702918765)  
- [_Salesforce Help: Standard Lightning Page Components_](https://help.salesforce.com/articleView?id=lightning_page_components.htm&language=en_US&_ga=2.168661153.1872851458.1702926453-1215546439.1702918765)  
- [_Salesforce Help: Flow Core Action: Send Custom Notification_](https://help.salesforce.com/s/articleView?id=sf.flow_ref_elements_actions_sendcustomnotification.htm&type=5&_ga=2.168661153.1872851458.1702926453-1215546439.1702918765)  
- [_Salesforce Help: Customize Onboarding with In-Dashboard Instructional Content_](https://help.salesforce.com/articleView?id=bi_onboarding_custom_dashboard_videos.htm&language=en_US&_ga=2.168661153.1872851458.1702926453-1215546439.1702918765)

## Promote Feature Adoption and Discovery

### Suitable Use Cases

Prompts and walkthroughs work best when you have something short and helpful to say, or when you want to quickly call attention to something new, interesting, or important. Prompts and walkthroughs help users quickly absorb and acknowledge information and then continue with their flow of work. These use cases are good candidates for prompts and walkthroughs.

- Features that are easy to learn and use immediately  
- Features that are available without setup or personalization  
- Features that are requested enhancements to existing functionality  
- Reminders or simple instructions to onboard to features that have low adoption  
- Tips for being productive in the app  

## Unsuitable Use Cases
Prompts and walkthroughs are less effective when you have lots of information to share, prerequisites to explain, or context to establish. These use cases aren’t suitable for prompts and walkthroughs.

- Features that are complex, with hard-to-remember workflows  
- Features that have a steep learning curve  
- Features that can be heavily personalized by users

### Consider Your Audience
In addition to the subject matter, consider the target audience for your prompt or walkthrough. Just like features, your users aren’t monolithic. They have a variety of experience levels, educational backgrounds, assumptions, and jobs to do. However, you can still develop prompts and walkthroughs that effectively support many types of users at once by remembering that most users:

- Know the basics, and don’t want their workflow interrupted without good reason  
- Want actionable, relevant information about updates to features they use often and new features that could increase productivity  
- Don’t want to be sold to, unless an offering is clearly tailored to their needs

### Prompt versus Walkthrough
A prompt is a single, small window that directs users’ attention to a feature, update, or call to action. The user notices the prompt, reads the information or takes action, and moves on with their day.
A walkthrough is a series of connected prompts that provides a step-by-step, guided experience across a single page or multiple pages for in-context learning. Walkthroughs ask more of the user’s time, attention, and action. However, the walkthrough’s unique hands-on experience encourages users to take the time to complete all steps.
Use a single prompt for a short message to help users quickly discover one feature. Use a walkthrough when you want to guide users through multiple steps that help them adopt the feature or to help users discover multiple related features.

A walkthrough is also a great resource for these activities:

- Onboarding new hires to their workspace  
- Providing a navigational or feature overview  
- Guiding users through a multi-step procedure

### Types of Prompts

| **Use Case**                                                                                    | **Floating Prompt** | **Targeted Prompt** | **Docked Prompt** |
| ----------------------------------------------------------------------------------------------- | ------------------- | ------------------- | ----------------- |
| Your goal is to drive readers to a resource, such as a training PDF or website.                 | :luc_check:         | :luc_check:         |                   |
| Your goal is to have readers acknowledge information without specifically completing an action. | :luc_check:         | :luc_check:         |                   |
| Your message is short (approximately one sentence).                                             | :luc_check:         | :luc_check:         |                   |
| You want to include information that the user can consult as they work.                         |                     |                     | :luc_check:       |
| You want to embed a video into the docked prompt.                                               |                     |                     | :luc_check:       |
| Your message is longer than one sentence.                                                       |                     |                     | :luc_check:       |

#### Floating Prompt:
A floating prompt is a non-intrusive way to nudge users toward a feature or opportunity. You can place a floating prompt in one of nine positions on a page.

- Top left  
- Top center  
- Top right  
- Middle left  
- Middle center  
- Middle right  
- Bottom left  
- Bottom center  
- Bottom right

#### Targeted Prompt:
Targeted prompts have all of the same benefits as a floating prompt without being confined to nine placement positions. Connect a targeted prompt to a specific page element to show your users exactly what you’re referring to.

#### Docked Prompt:
Docked prompts are helpful when users need to refer to content while exploring a feature on their own. Unlike the floating and targeted prompts, the docked prompt stays in place as the user navigates through the app. Use a docked prompt for content that you want to remain on screen, such as step-by-step instructions or an image or short video that users can follow in their flow of work. Consider using a docked prompt to display next steps or takeaways in the last step of a walkthrough.

### Resources

- [_Salesforce Help: In-App Guidance_](https://help.salesforce.com/articleView?id=customhelp_lexguid.htm&language=en_US&_ga=2.89186651.1905102893.1706640773-350744223.1706640773)  
- [_Video: Create Prompts in Lightning Experience_](https://salesforce.vidyard.com/watch/mfpLNa4prnDNuHS5zJm5wg?&_ga=2.89186651.1905102893.1706640773-350744223.1706640773&_gl=1*1w9oza2*_ga*MzUwNzQ0MjIzLjE3MDY2NDA3NzM.*_ga_H6M98GGB18*MTcwNjY0NTIwNy4yLjEuMTcwNjY0NTI2NC4wLjAuMA..*_gcl_au*NDYxMDU0NzQ1LjE3MDY2NDA3Nzc.)  
- [_Video: Create Walkthroughs in Lightning Experience_](https://salesforce.vidyard.com/watch/hXu7Vomp2bgPc5RSM1U6n3?&_ga=2.89186651.1905102893.1706640773-350744223.1706640773&_gl=1*1w9oza2*_ga*MzUwNzQ0MjIzLjE3MDY2NDA3NzM.*_ga_H6M98GGB18*MTcwNjY0NTIwNy4yLjEuMTcwNjY0NTI2NC4wLjAuMA..*_gcl_au*NDYxMDU0NzQ1LjE3MDY2NDA3Nzc.)
### Resources

- [_Salesforce Help: Create a Custom Report Type_](https://help.salesforce.com/s/articleView?id=sf.reports_defining_report_types.htm&type=5)  
- [_Salesforce Help: Considerations for Creating In-App Guidance_](https://help.salesforce.com/s/articleView?id=sf.customhelp_lex_prompt_consider.htm)  
- [_Salesforce Help: Analytics for In-App Guidance_](https://help.salesforce.com/articleView?id=customhelp_lex_prompt_monitor.htm)  
- [_Salesforce Help: PromptAction_](https://developer.salesforce.com/docs/atlas.en-us.224.0.object_reference.meta/api/sforce_api_objects_promptaction.htm)

