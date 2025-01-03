---
lab:
    title: 'Lab 5: Create a trigger-based journey'
---

## Lab 5: Create a trigger-based journey 

In this lab, you will learn how to:
- Create a journey based on a trigger
- Define exit criteria for the segment 

### Task 1: Create a trigger-based journey 
1. Navigate to the **Real-time journeys** work area.

1. Under **Engagement**, select **Journeys.**

1. Click **+New journey** in the command bar.

1. Select **Skip and create from blank.**

1. In **Name the journey**, enter **Welcome Journey.**

1. In **Choose journey** type, select **Trigger-based.**

1. In **Choose a trigger**, search for and select **Contact Created.**

1. Click **Create.**

1. From the Journey Settings on the right, in the Entry section, select **Add Condition.**

1. In the Attribute Drop-down menu, select **Contact created > Contact (Contact) > Account (Account) > Account Name.**

1. Change the operator to **Does not Equal.**

1. Set the value to **Humongous Insurance**. The condition should read **Account Name Does not Equal Humongous Insurance.**

1. Configure the rest of the items in the Entry section as follows:
    - In the Repeat section, select **Immediately.**
    - In the Time zone section, choose your time zone.
    - In Start, select today, 15 minutes from now.
    - In End, select tomorrow.

### Task 2: Define the journey goal
Next, we can identify the specific goal of the Customer Journey.  Goals help to identify what the end point of the journey is.  These can be things like driving a purchase or engaging with customers.  Providing a goal for the journey ensures that the journey is stopped once your objective has been met.    

For this journey, we are looking for a specific percentage of the people we are engaging with to click on a link that is in an email that we send them.  

1.	From the Journey settings on the right, navigate to the **Goal** section.

1.	In **The goal of this journey is**, select **Send a general notification.**

1. 	In **The goal is met when** field, select **A person clicked on at least one link.**

1.	In **The number of people needed**, enter **50**. Leave the **Percent** option selected. 

### Task 3: Define a frequency cap for the journey 
Contoso wants to ensure that they are not overwhelming their customers with commercial messages. To ensure that this does not happen, they want to apply a frequency cap to this journey.   

1.	From the Journey settings on the right, navigate to the **Other Settings** section.

1.	Under Frequency cap, make sure that **Apply frequency cap to this journey – skip commercial messages if cap is reached** is selected.  

1.	Under Maximum frequency across journeys, select **Go to frequency cap settings.** A new window will open.

1.	On the command bar, select **+New Setting.**

1.	In the Name field, enter **Contoso.**

1.	In the Maximum frequency per contact point section, configure based on the image below:

    ![Screenshot of the frequency cap settings, with Email set to Daily 3 and Monthly 10, text message set to Daily 1, Weekly 2, and Monthly 3. Nothing is set for push notification.](../media/frequency-cap.png)

1. Select **Save & Close** to save and close your new Frequency Cap settings.  

1.	Return to the window that contains your Welcome Journey. **Save** the journey and refresh your browser.

1.	From the Journey settings on the right, navigate to the **Other Settings** section again.

1.	Notice that the Contoso Frequency cap is now applied to this Journey.  

### Task 4: Build out the trigger-based journey 
Now that we have defined the necessary journey criteria, the next step is to build out the actual journey steps. 

1. In the journey designer, click the **plus icon (+)** under the Contact Created tile.

1. Select **Attribute Branch (Branch based on a specific value).**

1. In Display name on the right, enter **New Business Customer.**

1. Select **Branch 1** and in **Choose an attribute**, Search for **Description (description)** under Contact.

1. Change the value from Equals to **Contains.**

1. In Value, enter **Business.**

1. Click the **plus icon (+)** under Branch 1.

1. Select **Email: Send an email.**

1. In **Select email**, choose **Welcome Email 1.**

1. Click the **plus icon (+)** under the Send an email tile.

1. Select **Wait for Trigger.**

1. To configure the If/then branch, in the If/then branch panel on the right, under Wait for, Choose a branch condition type select The previous message gets an interaction.

1. In **Choose an interaction**, select **Email Link Clicked.**

1. In What’s the time limit?, enter **10 minutes.**

1. Back on the Journey diagram, to specify the link clicked, select **create branches.**

1. Select the attribute **Email Link Clicked.**

1. In Branch 1, select the call-to-action button from the email.

1. In the Yes path, click the **plus icon (+).**

1. Select **Send an email.**

1. In Select email, choose **Welcome Email 2.**

1. In the corresponding No path, click the **plus icon (+).**

1. Select **Send an email.**

1. In Select email, choose **Welcome Email 3.**

1. Save the journey.

1. Review the journey. Make any final changes.

1. Click **Publish.** Wait for the journey to publish.


