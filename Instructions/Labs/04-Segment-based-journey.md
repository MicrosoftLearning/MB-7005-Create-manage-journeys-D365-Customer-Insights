---
lab:
    title: 'Lab 4: Create a segment-based journey'
---
## Lab 4: Create a segment-based journey 

In this lab, you will learn how to:
- Create a journey based on a segment 
- Define exit criteria for the segment 

### Task 1: Create a segment-based journey 
Contoso wants to be able to engage with customers that meet specific demographic criteria. To accomplish this, they will create a segment-based journey.

1. Under Engagement, select **Journeys.**

1. Click **+New journey** in the command bar.

1. Select **Skip and create from blank.**

1. In Name the journey, enter **Seattle Campaign.**

1. In Choose journey type, select **Segment-based.**

1. In the Select a segment choose **Seattle Customers.**

1. In Select the frequency, choose **A repeating journey where all audience members repeat the journey every:**

1. Select **6 Weeks.**

1. Set the time zone to your time zone.

1. Set the Start date to today’s date, 30 minutes from now.

1. Set the End date to about six months from today.

1. Click **Create.**

1. From the Journey settings on the right ensure that you have the **Entry** section selected.

1. Go to the **Exclude by segments** and select **Business Customers.**

### Task 2: Define the journey exit criteria
Since the goal of this journey is to drive people to register for a marketing event, we want to ensure that once they register, no matter where they are in the journey, that the journey ends for them.  Additionally, if any Contoso employees live in Seattle, we want them to be aware of the upcoming event; however, we do not want them to go through the journey itself. For this reason, we are going limit who can continue the journey.  

1.	Select the **Exit** section.  

1.	Under the **Exit when a trigger occurs** section, select **Marketing Event Registration Created.**

1.	Select **Add condition.**

1.	Expand **Marketing event registration created**, and then expand **Marketing Event Reference.**

1.	Select **Event.**

    ![Screenshot of a list of exit criteria with Event selected.](../media/exit-criteria.png)

1.  Set the Operator to **Equals.**

1.	Set the Value to **Ted Contoso.**

1. In **Exit by segments**, set the value to **Contoso Customers.** Your exit criteria should look like the image below.

    ![Screenshot of exit criteria.](../media/complete-exit-criteria.png)

### Task 3: Build out the journey
Now that we have defined the different criteria related to this journey, we are going to create the journey itself.  

1. In the journey designer, click the **plus icon (+)** under the Contact Created tile.

1. Select **Attribute Branch (Branch based on a specific value).**

1. In Display name on the right, name the attrivute **New Business Customer.**

1. Select **Branch 1** and in Choose an attribute, Search for **Description (description)** under **Contact.**

1. Change the value from Equals to **Contains.**

1. In Value, enter **Business**.

1. Click the **plus icon (+)** under Branch 1.

1. Select **Email: Send an email.**

1. In Select email, choose **Welcome Email 1.**

1. Click the **plus icon (+)** under the Send an email tile.

1. Select **Wait for Trigger.**

1. In the If/then branch panel on the right, under Wait for, choose a branch condition type select **The previous message gets an interaction.**

1. In Choose an interaction, select **Email Link Clicked.**

1. In What’s the time limit?, enter **10 minutes.**

1. Back on the Journey diagram, to specify the link clicked, select **create branches.**

1. Select the attribute **Email Link Clicked.**

1. In Branch 1, Choose a link, select the call-to-action button from the email.

1. Underneath the button clicked path, click the **plus icon (+).**

1. Select **Send an email.**

1. In Select email, choose **Welcome Email 2.**

1. In the corresponding No path, click the **plus icon (+).**

1. Select **Send an email.**

1. In Select email, choose **Welcome Email 3.**

1. Save the journey.

1. Review the journey. Make any final changes.

1. Click **Publish**. Wait for the journey to publish.

